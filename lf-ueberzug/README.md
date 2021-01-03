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
see `lf-shellcd`, which is part of this repository. `lf-ueberzug` is fully
compatible with `lf-shellcd`.


## Installation

Prerequisites:
+ ueberzug
+ imagemagick (for .svg previews)
+ ffmpeg (for video file thumbnails)
+ gs (for pdf previews)

```
# Install files (mind the 'sudo -E')
sudo -E make install
```
