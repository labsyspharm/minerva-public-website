---
layout: default
title: Minerva on the Command Line
parent: How to Use Minerva
nav_order: 90
---
# Minerva on the Command Line

Follow step-by-step instructions [here](https://github.com/labsyspharm/minerva-story/wiki/How-to-run-Minerva-Author%3F-(from-source-code)) on how to download, install and get started using <span style="color: #278AB0;">**Minerva Author**</span> on the command line.

## Syntax

```
uv run minerva-author-render [-h] [--threads N] [--url URL] [--vis DIR] [--no-images] [--force] OME_TIFF AUTHOR_JSON OUTPUT_DIR

positional arguments:
  OME_TIFF     Input path to OME-TIFF with all channel groups
  AUTHOR_JSON  Input Minerva Author save file with channel configuration
  OUTPUT_DIR   Output directory for exhibit and rendered JPEG pyramid

options:
  -h, --help   show this help message and exit
  --threads N  Number of worker threads to process data in parallel (default: 1)
  --url URL    URL of planned hosting location of rendered JPEG pyramid
  --vis DIR    Input data visualization directory (default constructed from author .json)
  --no-images  Do not generate JPEG tiles (but do build everything else)
  --force      Overwrite output
```
