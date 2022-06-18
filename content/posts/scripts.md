---
title: "miscellaneous useful scripts"
date: 2022-05-29T18:42:26+03:00
draft: false
---

### Convert a folder of mp3 files to opus for audiobooks

windows:

```cmd
for %i in (*.mp3) do ffmpeg -i "%i" -c:a libopus -b:a 32k "%~ni.ogg"
```

linux:

```bash
for f in *.mp3; do ffmpeg -i "${f}" -c:a libopus -b:a 32k "${f%%.*}.ogg"; done
```

### JPEG to JPEG XL

windows:

```cmd
for %i in (*.jpg) do cjxl "%i" "%~ni.jxl"
```

linux:

```bash
for f in *.jpg; do cjxl "${f}" "${f%%.*}.jxl"; done
```

### Download youtube playlist using yt-dlp with index in filename

```bash
yt-dlp -f "bestvideo[height<=1080]+bestaudio" -o "%(playlist_index)s-%(title)s.%(ext)s" playlist_link
```

### Other FFmpeg stuff

```bash
# webm -> ogg (containing opus from yt-dlp)
ffmpeg -i input.webm -acodec copy output.ogg
# any container to webm/mkv
ffmpeg -i input.mp4 -acodec copy -vcodec copy output.webm
# trim any video without encoding
ffmpeg -ss 00:00:00 -i input.mp4 -to 00:00:00 -c copy output.mp4
# av1
ffmpeg -i input.mp4 -vcodec libsvtav1 -acodec copy output.mkv
```
