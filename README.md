# KatApp Documentation

![example workflow](https://github.com/kat-app/katapp-docs/actions/workflows/hugo-deploy.yaml/badge.svg)

<img src="./static/katapp-logo.png" width="125">

---

This repository contains the end user documentation for *KatApp*. It is intended to provide general instructions for users of the *KatApp* app and the *KatApp* dashboard.

It does not contain technical documentation. If you're interested in the technical details of the *KatApp* ecosystem, have a look at the separate repositories for the app, the dashboard and the backend.

---

## Introduction

This documentation is build with *hugo*, an open-source static website generator.

Checkout *hugo*: https://gohugo.io/

## Getting started

To build and serve the documentation locally, an installation or an executable of *hugo* is required. For installation instructions, follow the official *hugo* manual: https://gohugo.io/installation/

To serve the site locally, run the following command:

```sh
$ hugo serve
```

To build the site, run the following command:

```sh
$ hugo --gc --minify
```

## Writing documentation

### Contents

The documentation is written using *Markdown*. All the contents of the documentation site are located within the `./content` directory. The content is separated into several languages. Every language directory should follow exactly the same layout.

Example page:

```
---
title: Sample
geekdocNav: true
geekdocAlign: left
geekdocAnchor: false
---

# Sample header

This is some sample content ...
```

### Menu

The documentation menu structure is represented by a collection of separate configuration files. To customize the main menu structure, edit the following file: `./data/menu/main.yaml`

Example menu:

```yml
main:
  - name:
      en: English title
      de: German title
    sub:
      - name:
          en: English subtitle
          de: German subtitle
        ref: '/page/ref'
```

### Assets

All assets, such as images, should be located in the `./static` directory.

Example structure:

```
static/
├── logo.png
├── info.pdf
└── ...
```