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
python render.py [-h] [--url url] [--vis vis] [--force] ome_tiff author_json output_dir

positional arguments
  ome_tiff      Input path to OME-TIFF with all channel groups
  author_json   Input Minerva Author save file with channel configuration
  output_dir    Output directory for exhibit and rendered JPEG pyramid

options:
  -h, --help    show this help message and exit
  --url url     URL to planned hosting location of rendered JPEG pyramid
  -vis vis      Input data visualization directory (default constructed from author .json)
  --force       Overwrite output
```