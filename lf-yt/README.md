# Preview and Download Youtube Search Results with **lf**

![](demo.gif)

Given an input `lf-yt` searches Youtube and, showing video thumbnails, allows
to select videos for preview and download. Downloads are saved to *~/.lf-yt*.

## Usage

Export your Youtube API-key to the environment variable *YT_API_KEY* or store it inside
the file *~/.youtube.apikey*. Then run a search query, e.g. `lf-yt Chopin`.

## Installation

Prerequisites:

+ A youtube API-key
+ `ueberzug`
+ `mpv`
+ `youtube-dl`

```
# Install files (mind the 'sudo -E')
sudo -E make install
```
