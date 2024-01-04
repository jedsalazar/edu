---
title: "ml-metadata-store-server Image Variants"
type: "article"
unlisted: true
description: "Detailed information about the public ml-metadata-store-server Chainguard Image variants"
date: 2023-12-13 00:32:10
lastmod: 2023-12-13 00:32:10
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
weight: 550
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=false url="/chainguard/chainguard-images/reference/ml-metadata-store-server/" >}}
{{< tab title="Variants" active=true url="/chainguard/chainguard-images/reference/ml-metadata-store-server/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/ml-metadata-store-server/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/ml-metadata-store-server/provenance_info/" >}}
{{</ tabs >}}

This page shows detailed information about all public variants of the Chainguard **ml-metadata-store-server** Image.

## Variants Compared
The **ml-metadata-store-server** Chainguard Image currently has 2 public variants: 

- `latest-dev`
- `latest`

The table has detailed information about each of these variants.

|              | latest-dev                       | latest                           |
|--------------|----------------------------------|----------------------------------|
| Default User | `nonroot`                        | `nonroot`                        |
| Entrypoint   | `/usr/bin/metadata_store_server` | `/usr/bin/metadata_store_server` |
| CMD          | not specified                    | not specified                    |
| Workdir      | not specified                    | not specified                    |
| Has apk?     | yes                              | no                               |
| Has a shell? | yes                              | no                               |

Check the [tags history page](/chainguard/chainguard-images/reference/ml-metadata-store-server/tags_history/) for the full list of available tags.

## Packages Included
The table shows package distribution across variants.

|                            | latest-dev | latest |
|----------------------------|------------|--------|
| `apk-tools`                | X          |        |
| `bash`                     | X          |        |
| `busybox`                  | X          |        |
| `ca-certificates-bundle`   | X          | X      |
| `git`                      | X          |        |
| `glibc`                    | X          | X      |
| `glibc-locale-posix`       | X          | X      |
| `ld-linux`                 | X          | X      |
| `libbrotlicommon1`         | X          |        |
| `libbrotlidec1`            | X          |        |
| `libcrypt1`                | X          |        |
| `libcrypto3`               | X          |        |
| `libcurl-openssl4`         | X          |        |
| `libexpat1`                | X          |        |
| `libgcc`                   | X          | X      |
| `libnghttp2-14`            | X          |        |
| `libpcre2-8-0`             | X          |        |
| `libssl3`                  | X          |        |
| `libstdc++`                | X          | X      |
| `ml-metadata-store-server` | X          | X      |
| `ncurses`                  | X          |        |
| `ncurses-terminfo-base`    | X          |        |
| `openssl-config`           | X          |        |
| `wolfi-baselayout`         | X          | X      |
| `zlib`                     | X          |        |
