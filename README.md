# Pandoc/python static site generator

The best of python, pandoc (haskell) and shell all in one. Should work with a standard full python installation without requiring `pip install`. Made for ease of use and development due to python's built in string manipulation functions. Pandoc and python are widely used hopefully lending to the longevity of this code.

## Features
- RSS feed generated with item for each page.
- 1 folder deep folder structure is transformed into categorised pages. See example below.
- Write pages in pandoc markdown.

## Requirements
- Python3.\*
- A Linux shell. Tested on ubuntu and ubuntu for WSL. Should work on most Linux distros.
- Pandoc. `sudo apt install pandoc` if debian based.

## Example setup

For example create directory of directories with this structure. Each post can be put within a folder which is it's category. The generator will then simply create an index of each post within each category and display this as a list.
```
python3 generate.py

# Here is an example src directory. The home page is the index.md file.

src
├── index.md
├── art
│   └── artist_page.md
└── maths
    └── my_favourite_maths.md

```
Run `python3 -m http.server` in the site directory to view the site on a local server.

Each markdown must contain the following at the top of the file:

```
---
lang: en-GB
title: Title for page
description: Some description

---
```
