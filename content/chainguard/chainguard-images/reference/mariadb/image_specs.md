---
title: "mariadb Image Details"
type: "article"
unlisted: true
description: "Detailed information about the public mariadb Chainguard Image."
date: 2023-03-07T11:07:52+02:00
lastmod: 2024-03-01 12:14:22
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
weight: 550
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=false url="/chainguard/chainguard-images/reference/mariadb/" >}}
{{< tab title="Details" active=true url="/chainguard/chainguard-images/reference/mariadb/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/mariadb/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/mariadb/provenance_info/" >}}
{{</ tabs >}}

This page shows detailed information about the Chainguard **mariadb** Image.

|              | latest-dev                                     | latest                                         |
|--------------|------------------------------------------------|------------------------------------------------|
| Default User | `mysql`                                        | `mysql`                                        |
| Entrypoint   | `/usr/local/bin/docker-entrypoint.sh mariadbd` | `/usr/local/bin/docker-entrypoint.sh mariadbd` |
| CMD          | not specified                                  | not specified                                  |
| Workdir      | not specified                                  | not specified                                  |
| Has apk?     | yes                                            | no                                             |
| Has a shell? | yes                                            | yes                                            |

Check the [tags history page](/chainguard/chainguard-images/reference/mariadb/tags_history/) for the full list of available tags.

## Packages Included
The table shows package distribution across variants.

|                               | latest-dev | latest |
|-------------------------------|------------|--------|
| `apk-tools`                   | X          |        |
| `bash`                        | X          | X      |
| `busybox`                     | X          | X      |
| `ca-certificates-bundle`      | X          | X      |
| `chainguard-baselayout`       | X          | X      |
| `git`                         | X          |        |
| `glibc`                       | X          | X      |
| `glibc-locale-posix`          | X          | X      |
| `ld-linux`                    | X          | X      |
| `libaio`                      | X          | X      |
| `libbrotlicommon1`            | X          |        |
| `libbrotlidec1`               | X          |        |
| `libcrypt1`                   | X          | X      |
| `libcrypto3`                  | X          | X      |
| `libcurl-openssl4`            | X          |        |
| `libexpat1`                   | X          |        |
| `libgcc`                      | X          | X      |
| `libidn2`                     | X          |        |
| `libnghttp2-14`               | X          |        |
| `libpcre2-8-0`                | X          | X      |
| `libpsl`                      | X          |        |
| `libssl3`                     | X          | X      |
| `libstdc++`                   | X          | X      |
| `libunistring`                | X          |        |
| `linux-pam`                   | X          | X      |
| `mariadb-10.11`               | X          | X      |
| `mariadb-11.2-oci-entrypoint` | X          | X      |
| `ncurses`                     | X          | X      |
| `ncurses-terminfo-base`       | X          | X      |
| `openssl-config`              | X          | X      |
| `pwgen`                       | X          | X      |
| `tzdata`                      | X          | X      |
| `wget`                        | X          |        |
| `wolfi-baselayout`            | X          | X      |
| `xz`                          | X          | X      |
| `zlib`                        | X          | X      |

