# KatApp Documentation

![example workflow](https://github.com/kat-app/katapp-docs/actions/workflows/hugo-deploy.yaml/badge.svg)

---

This repository contains the end user documentation for *KatApp*. It is intended to provide general instructions for users of the *KatApp* app and the *KatApp* dashboard.

It does not contain technical documentation. If you're interested in the technical details of the *KatApp* ecosystem, have a look at the separate repositories for the app, the dashboard and the backend.

---

## Introduction

This documentation is build with [hugo](https://gohugo.io/), an open-source static website generator.

## Getting started

### Development

To build and serve the documentation locally, an installation or an executable of *hugo* is required. For installation instructions, follow the official [hugo manual](https://gohugo.io/installation/).

To serve the site locally, run the following command:

```sh
$ hugo server --buildDrafts
```

Alternatively, you can use the launch task "Debug Hugo Docs" under VsCode.

### Deploy

To build the site, run the following command:

```sh
$ hugo --gc --minify
```

## Writing documentation

### Contents

The documentation is written using *Markdown*. All the contents of the documentation site are located within the `./content` directory.

The documentation is written in only in English.

We use the open source [Relearn theme](https://github.com/McShelby/hugo-theme-relearn) for Hugo. You can find instructions on how to write and style Hugo pages on the [official Hugo website](https://gohugo.io/getting-started/quick-start/) or on the [official website of the Relearn theme](https://mcshelby.github.io/hugo-theme-relearn/).