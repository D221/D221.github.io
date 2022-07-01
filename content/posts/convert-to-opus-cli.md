---
title: " convopus"
date: 2022-05-29T18:06:31+03:00
draft: false
cover:
    image: "/img/convert-to-opus-cli-static.png"
---
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/D221/convopus?label=Download)](https://github.com/D221/convopus/releases/latest)
![GitHub](https://img.shields.io/github/license/D221/convopus)
![GitHub Workflow Status](https://img.shields.io/github/workflow/status/D221/convopus/Pylint)

convopus is a Python CLI program for converting audio files to [opus](https://opus-codec.org/) audio format.

slightly outdated demo:
{{< rawhtml >}}
    <video
              src="/img/convert-to-opus-cli.webm"
              alt="convert-to-opus demo"
              autoplay
              loop
              muted
              playsinline>
    </video>
{{< /rawhtml >}}

## Features

- Windows / Linux / macOS / Android (via Termux) support
- Customizable bitrate and more (via config.json)
- Support of various audio formats / containers

## Installation

Must have installed ffmpeg and added to PATH

```bash
pip install -U convopus
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

Also you can find windows binary in [Releases](https://github.com/D221/convopus/releases/latest)

You can customize settings in **config.json** located in:

|OS|config.json location|
|-|-|
|Windows|%LocalAppData%\D221\convopus|
|Linux|~/.config/convopus|
|macOS|~/Library/Application Support/convopus|

## License

[MIT](https://choosealicense.com/licenses/mit/)
