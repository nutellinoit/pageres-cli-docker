# Pageres-cli Docker image

Original project : https://github.com/sindresorhus/pageres-cli

```bash
make build
```

Add alias on `~/.bashrc` or `~/.zshrc`: `alias pageres='docker run --rm -it -v ${PWD}:/tmp/ nutellinoit/pageres'`

Use `pageres` command.

Examples:

```bash
~ pageres
  Capture website screenshots

  Specify urls and screen resolutions as arguments. Order doesn't matter.
  Group arguments with [ ]. Options defined inside a group will override the outer ones.
  Screenshots are saved in the current directory.

  Usage
    pageres <url> <resolution>
    pageres [ <url> <resolution> ] [ <url> <resolution> ]

  Example
    pageres todomvc.com yeoman.io 1366x768 1600x900
    pageres todomvc.com yeoman.io 1366x768 1600x900 --overwrite
    pageres [ yeoman.io 1366x768 1600x900 --no-crop ] [ todomvc.com 1024x768 480x320 ] --crop
    pageres todomvc.com 1024x768 --filename='<%= date %> - <%= url %>'
    pageres yeoman.io 1366x768 --selector='.page-header'
    pageres unicorn.html 1366x768

  Options
    -v, --verbose            Verbose output
    -c, --crop               Crop to the set height
    -d, --delay=<seconds>    Delay screenshot capture
    --filename=<template>    Custom filename
    --overwrite              Overwrite file if it exists
    --selector=<element>     Capture DOM element
    --hide=<element>         Hide DOM element (Can be set multiple times)
    --cookie=<cookie>        Browser cookie (Can be set multiple times)
    --header=<string>        Custom HTTP request header (Can be set multiple times)
    --username=<username>    Username for HTTP auth
    --password=<password>    Password for HTTP auth
    --scale=<number>         Scale webpage
    --format=<string>        Image format
    --css=<string>           Apply custom CSS

  <url> can also be a local file path.
```
