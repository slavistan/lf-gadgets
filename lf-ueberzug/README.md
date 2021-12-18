# Set up **lf** File Previews With **ueberzug**

![](demo.gif)

`lf-ueberzug` will preview images, documents and video thumbnails with `ueberzug`. Preview behavior can be extend or adjusted in *lf-ueberzug-previewer*.

## Usage

Run `./lf-ueberzug`. Optionally, a startup directory can be specified. By default, `lf-ueberzug` will launch inside the *examples* directory. No installation is required.

**Prerequisites**

+ `zsh` for scripting
+ `ueberzug` for all graphical previews
+ `graphicsmagick` for svg and gif previews
+ `ffmpeg` for video file thumbnails
+ `gs` for PDF previews

For shell integration symlink `lf-ueberzug` into */usr/local/bin* and `alias lf=lf-ueberzug` in your shell configuration. This can be combined with the functionality of `lf-shellcd`, which is part of this directory, to change your working directory upon exiting.