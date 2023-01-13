---
layout: archive
title: "Random"
permalink: /random/
author_profile: true
---

{% include base_path %}

Some useful things (to me, not necessarily to you) I keep having to redo because they get lost in spacetime. All credit goes to the brave souls at StackOverflow.

# Bash

## Compressing all pdfs in a folder (and subfolder) 

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
  # Compress. You can also try {screen,ebook,default} instead of printer.
  ps2pdf -dPDFSETTINGS=/printer ${fnoe}_bckup.pdf $f
done
```
## Replace file contents

Did your e-mail change and how you have to search through all [manifests](https://wiki.ros.org/Manifest) to replace it with the new one? Fear not. 

You can replace string `A` with string `B` within all files, folders, and subfolders by using some regex magic, as follows.

```sh
find . -type f -exec sed -i'' -e 's/A/B/g' {} +
```

## Rename all files using

New prefix for all the libraries you have? No worries. Based on [this](https://stackoverflow.com/questions/16541582/find-multiple-files-and-rename-them-in-linux) and [this](https://stackoverflow.com/questions/1961255/rename-files-using-a-regex-with-bash) and [this](https://unix.stackexchange.com/questions/141086/how-can-i-use-rename-to-recursively-rename-everyting-to-uppercase) and maybe some others.

Rename all folders and files by replacing substring `A` to `B` using regex magic.

```sh
find . -type f -execdir rename 's/A/B/g' {} +
```

## "Uninstalling" a cmake installed package

CMake installations create a file `install_manifest.txt` with all the installed file locations. You can remove them all with. 

```sh
sudo xargs rm < install_manifest.txt
```

## Running a command on a set of folders

For instance, `git pull` is all subfolders.

```sh
for d in */ ; do
    echo "Git pull in $d..."
    cd "$d"
    git pull
    cd ..
done
```

## Example tab using HTML and Javascript

From: https://www.w3schools.com/howto/tryit.asp?filename=tryhow_js_tabs_open

<p>In this example, we use JavaScript to "click" on the London button, to open the tab on page load.</p>

<div class="tab">
  <button class="tablinks" onclick="openCity(event, 'London')" id="defaultOpen">London</button>
  <button class="tablinks" onclick="openCity(event, 'Paris')">Paris</button>
  <button class="tablinks" onclick="openCity(event, 'Tokyo')">Tokyo</button>
</div>

<div id="London" class="tabcontent">
  <h3>London</h3>
  <p>London is the capital city of England.</p>
</div>

<div id="Paris" class="tabcontent">
  <h3>Paris</h3>
  <p>Paris is the capital of France.</p> 
</div>

<div id="Tokyo" class="tabcontent">
  <h3>Tokyo</h3>
  <p>Tokyo is the capital of Japan.</p>
</div>

<script>
function openCity(evt, cityName) {
  var i, tabcontent, tablinks;
  tabcontent = document.getElementsByClassName("tabcontent");
  for (i = 0; i < tabcontent.length; i++) {
    tabcontent[i].style.display = "none";
  }
  tablinks = document.getElementsByClassName("tablinks");
  for (i = 0; i < tablinks.length; i++) {
    tablinks[i].className = tablinks[i].className.replace(" active", "");
  }
  document.getElementById(cityName).style.display = "block";
  evt.currentTarget.className += " active";
}

// Get the element with id="defaultOpen" and click on it
document.getElementById("defaultOpen").click();
</script>
