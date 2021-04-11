# Set up **lf** File Previews With **ueberzug**

![](demo.gif)

Installs `lf-ueberzug` which sets up `lf` to preview images, documents and
video thumbnails with `ueberzug`. Preview behavior can be extend or adjusted in
*lf-ueberzug-previewer*.


## Usage

```
lf-ueberzug
```

For comfy shell integration simply `alias lf=lf-ueberzug` or, if you'd
additionally like to change your shell's working directory upon exiting `lf`,
see `lf-shellcd`, which is part of this repository.


## Installation

Prerequisites:
+ ueberzug
+ graphicsmagick (for svg and gif previews)
+ ffmpeg (for video file thumbnails)
+ gs (for pdf previews)

```
# copy scripts into $PATH
sudo cp -t /usr/local/bin lf-ueberzug lf-ueberzug-cleaner lf-ueberzug-previewer

# copy config file
mkdir -p "${XDG_CONFIG_HOME:-$HOME/.config}/lf-ueberzug"
cp lfrc-ueberzug "${XDG_CONFIG_HOME:-$HOME/.config}/lf-ueberzug"
```

To uninstall simply delete the files.
