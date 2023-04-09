---
title: "miscellaneous useful scripts"
date: 2022-05-29T18:42:26+03:00
draft: false
---

### Convert a folder of mp3 files to opus for audiobooks

```bash
convopus "input_folder" -b 32k
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

### H.264 to AV1
windows:

```cmd
for %i in (*.mp4) do ffmpeg -i "%i" -vcodec libsvtav1 -acodec libopus "%~ni.mkv"
```

linux:

```bash
for f in *.mp4; do ffmpeg -i "${f}" -vcodec libsvtav1 -acodec libopus "${f%%.*}.mkv"; done
```

### SOCKS5 Python Proxy Checker
https://gist.github.com/D221/b77f09eea1098951b2420de3bc292005


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
