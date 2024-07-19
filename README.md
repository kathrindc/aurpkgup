# aurpkgup - a minimal AUR helper

`aurpkgup` is pretty simple. It doesn't automate the build process, it doesn't download anything, it just lets you know if anything needs updating.

This script was created, because I just want to know if any of my AUR packages are out-of-date and I need to re-build them. I don't use a full-featured AUR wrapper like `yay` or `pikaur` because I just don't need it.

## Installation

Install [jq](https://archlinux.org/packages/extra/x86_64/jq/) (used to parse AUR RPC responses) as such:

```sh
$ sudo pacman -Sy jq
```

Then just download the script into your user's local bin folder and mark it as executable:

```sh
$ curl -o ~/.local/bin/aurpkgup 'https://raw.githubusercontent.com/kathrindc/aurpkgup/main/aurpkgup'
$ chmod u+x ~/.local/bin/aurpkgup
```

## Usage

Use an editor of your choice to edit the file `~/.config/aurpkgup` and write all the packages you want the script to check for you into individual lines. For example:

```
xivlauncher-git
pcsx2-latest-bin
socranop
```

Save the file and quit the editor. Now you can just run `aurpkgup` to check if any of your packages need updating.

