---
title: " convopus"
date: 2022-05-29T18:06:31+03:00
draft: false
cover:
    image: "/img/convopus-static.png"
---
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/D221/convopus?label=Download)](https://github.com/D221/convopus/releases/latest)
![GitHub](https://img.shields.io/github/license/D221/convopus)
![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/D221/convopus/pylint.yml?branch=main)


convopus is a Python CLI program for converting audio files to [opus](https://opus-codec.org/) audio format.

{{< rawhtml >}}
    <video
              src="/img/convopus.webm"
              alt="convopus demo"
              autoplay
              loop
              muted
              playsinline>
    </video>
{{< /rawhtml >}}

## Features

- Windows / Linux / macOS / Android (via Termux) support
- Customizable bitrate, vbr and more (via config.json)
- Support of various input audio formats / containers
- Fast multi threading converting
- Recursive conversion

## Installation

Must have installed ffmpeg and added to PATH

```bash
pip install convopus
```

## Build

```bash
git clone https://github.com/D221/convopus
cd convopus
pip install .
```

## Usage

```bash
convopus -h # for info
# The pogram detects directory or file
convopus /path/to/directory
convopus /path/to/file
```

You can customize settings in **config.json** located in:

|OS|config.json location|
|-|-|
|Windows|%LocalAppData%\D221\convopus|
|Linux|~/.config/convopus|
|macOS|~/Library/Application Support/convopus|

## License

[MIT](https://choosealicense.com/licenses/mit/)
