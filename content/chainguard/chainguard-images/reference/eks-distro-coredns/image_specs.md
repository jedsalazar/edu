---
title: "eks-distro-coredns Image Details"
type: "article"
unlisted: true
description: "Detailed information about the public eks-distro-coredns Chainguard Image."
date: 2024-03-01 12:14:22
lastmod: 2024-03-01 12:14:22
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
weight: 550
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=false url="/chainguard/chainguard-images/reference/eks-distro-coredns/" >}}
{{< tab title="Details" active=true url="/chainguard/chainguard-images/reference/eks-distro-coredns/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/eks-distro-coredns/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/eks-distro-coredns/provenance_info/" >}}
{{</ tabs >}}

This page shows detailed information about the Chainguard **eks-distro-coredns** Image.

|              | latest-dev                      | latest                          |
|--------------|---------------------------------|---------------------------------|
| Default User | `nonroot`                       | `nonroot`                       |
| Entrypoint   | `/usr/bin/coredns -dns.port=53` | `/usr/bin/coredns -dns.port=53` |
| CMD          | not specified                   | not specified                   |
| Workdir      | not specified                   | not specified                   |
| Has apk?     | yes                             | no                              |
| Has a shell? | yes                             | no                              |

Check the [tags history page](/chainguard/chainguard-images/reference/eks-distro-coredns/tags_history/) for the full list of available tags.

## Packages Included
The table shows package distribution across variants.

|                          | latest-dev | latest |
|--------------------------|------------|--------|
| `apk-tools`              | X          |        |
| `bash`                   | X          |        |
| `busybox`                | X          |        |
| `ca-certificates-bundle` | X          | X      |
| `chainguard-baselayout`  | X          | X      |
| `eks-distro-coredns-1.9` | X          | X      |
| `git`                    | X          |        |
| `glibc`                  | X          | X      |
| `glibc-locale-posix`     | X          | X      |
| `ld-linux`               | X          | X      |
| `libbrotlicommon1`       | X          |        |
| `libbrotlidec1`          | X          |        |
| `libcrypt1`              | X          |        |
| `libcrypto3`             | X          |        |
| `libcurl-openssl4`       | X          |        |
| `libexpat1`              | X          |        |
| `libidn2`                | X          |        |
| `libnghttp2-14`          | X          |        |
| `libpcre2-8-0`           | X          |        |
| `libpsl`                 | X          |        |
| `libssl3`                | X          |        |
| `libunistring`           | X          |        |
| `ncurses`                | X          |        |
| `ncurses-terminfo-base`  | X          |        |
| `openssl-config`         | X          |        |
| `wget`                   | X          |        |
| `wolfi-baselayout`       | X          | X      |
| `zlib`                   | X          |        |

