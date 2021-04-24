# Scrolling and Pagination for **lf** File Previews

![](demo.gif)

Proof-of-concept setup to enable scrolling up and down previews. A file is used to store the current preview offset (i.e. line of file, document page, frame of gif, ..). The file path is communicated to `lf` via an environment variable, which is accessible to shell commands inside `lf` which increase or decrease the value.

For the sake of simplicity this script only implements scrolling for text documents. However, the same configuration can be expanded to navigate pages of a pdf, frames of a gif, etc.

## Usage

```
lf-scrollingpreview
```

Use `>` and `<` to scroll down or up, respectively.

## Installation

```
# copy scripts into $PATH
sudo cp lf-scrollingpreview lf-scrollingpreview-previewer /usr/local/bin
sudo chmod 755 /usr/local/bin/lf-scrollingpreview /usr/local/bin/lf-scrollingpreview-previewer

# copy config file
mkdir -p "${XDG_CONFIG_HOME:-$HOME/.config}/lf-scrollingpreview"
cp lfrc-scrollingpreview "${XDG_CONFIG_HOME:-$HOME/.config}/lf-scrollingpreview"
```

To uninstall simply delete the files.
