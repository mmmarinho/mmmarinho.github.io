---
layout: archive
title: "Random"
permalink: /random/
author_profile: true
---

{% include base_path %}

Some useful things (to me, not necessarily to you) I keep having to redo because they get lost in spacetime.

# Compressing all pdfs in a folder (and subfolder) using `bash`

In a recent version of the `ghostscript` (or `gs` for close friends), a script I have always used stopped working, so here's what I've been doing.
This works for Ubuntu (including the Linux subsystem version in Windows 11).

```sh
#!/bin/bash
for f in $(find . -name '*.pdf')
do 
  echo "Processing $f"
  # Grab filename without extension (just whatever comes before the first .)
  # might fail for other purposes, but works fine for .pdfs
  fnoe="${f%.*}"
  # Backup original file. This will also automatically backup any existing
  # backups so it's mostly safe.
  mv $f ${fnoe}_bckup.pdf
  # Convert to .ps
  pdf2ps ${fnoe}_bckup.pdf ${fnoe}.ps
  # Convert back to .pdf
  ps2pdf -dPDFSETTINGS=/printer ${fnoe}.ps $f
done
```

