# Scrolling and Pagination for **lf** File Previews

![](demo.gif)

Proof-of-concept setup to enable scrolling up and down previews of text files. A temporary file is used to store the current preview offset, i.e. the line number or the document page etc. This file's location is communicated to `lf` via an environment variable which is also accessible to shell commands inside `lf` to increase or decrease the value. The previewer script respects the offset value and shifts the view accordingly.

For the sake of clarity this gadget only implements scrolling of text previews. If graphical previews are set up the very same configuration can be used to navigate pages of a pdf or frames of a gif.

## Usage

Launch `lf-scrollingpreview` in a terminal, navigate to a text file and use `>` and `<` to scroll down or up, respectively.

## Installation

From inside this subdirectory run these instructions as a regular user:

```
sudo cp lf-scrollingpreview lf-scrollingpreview-previewer /usr/local/bin
mkdir -p "$HOME/.config/lf-scrollingpreview"
cp lfrc-scrollingpreview "$HOME/.config/lf-scrollingpreview"
```

This will yield the following directory structure:

```
 /usr/local/bin
├─  lf-scrollingpreview
└─  lf-scrollingpreview-previewer

 $HOME/.config
└─  lf-scrollingpreview
   └─  lfrc-scrollingpreview
```

To **uninstall** simply delete the newly created files.
