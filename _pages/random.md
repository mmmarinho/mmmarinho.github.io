---
layout: archive
title: "Random"
permalink: /random/
author_profile: true
---

{% include base_path %}

Some useful things (to me, not necessarily to you) I keep having to redo because they get lost in spacetime. All credit goes to the brave souls at StackOverflow.

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
# Replace file contents using `bash`

Did your e-mail change and how you have to search through all [manifests](https://wiki.ros.org/Manifest) to replace it with the new one? Fear not. 

You can replace string `A` with string `B` within all files, folders, and subfolders by using some regex magic, as follows.

```sh
find . -type f -exec sed -i'' -e 's/A/B/g' {} +
```

# Rename all files using `bash`

New prefix for all the libraries you have? No worries. Based on [this](https://stackoverflow.com/questions/16541582/find-multiple-files-and-rename-them-in-linux) and [this](https://stackoverflow.com/questions/1961255/rename-files-using-a-regex-with-bash) and [this](https://unix.stackexchange.com/questions/141086/how-can-i-use-rename-to-recursively-rename-everyting-to-uppercase) and maybe some others.

Rename all folders and files by replacing substring `A` to `B` using regex magic.

```sh
find . -type f -execdir rename 's/A/B/g' {} +
```

# "Uninstalling" a cmake installed package

```sh
sudo xargs rm < install_manifest.txt
```
