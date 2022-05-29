---
title: "convert-to-opus"
date: 2022-05-28T01:10:32+03:00
draft: false
cover:
    image: "/img/windows.png"
---

## Also check out CLI of this [convert-to-opus-cli]({{< ref "/posts/convert-to-opus-cli" >}})

convert_to_opus is a Python GUI program for converting audio file directories to [opus](https://opus-codec.org/) audio format.

## Features

- You can choose whether or not you want to preserve the original files
- The ability to choose the bitrate
- The majority of commonly used audio file forms are supported

## Screenshots

![ScreenShot1](/img/convert-to-opus-windows.png)

![ScreenShot2](/img/convert-to-opus-linux.png)

## Installation

```bash
pip install convert_to_opus
```

## Requirements

- ffmpeg
- Python >=3.7
- wxPython

## Usage

```bash
convert_to_opus
```

Choose a directory then press CONVERT.

## License

[MIT](https://choosealicense.com/licenses/mit/)
