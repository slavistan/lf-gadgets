# Preview and Download Youtube Search Results with **lf**

![](demo.gif)

Given an input `lf-yt` searches Youtube and, showing video thumbnails, allows to select videos for preview and download. Downloads are saved to *~/.lf-yt* by default.

## Usage

Export your Youtube API-key to the environment variable *YT_API_KEY* or store it inside the file *~/.youtube.apikey*. Then open a terminal and run a search query, e.g. `./lf-yt Chopin`. No installation is required.

**Prerequisites**

+ A youtube API-key
+ `zsh` for scripting
+ `ueberzug` for video thumbnail previews
+ `mpv` to watch a video
+ `youtube-dl` to download videos