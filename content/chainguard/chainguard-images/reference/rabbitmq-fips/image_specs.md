---
title: "rabbitmq-fips Image Details"
type: "article"
unlisted: true
description: "Detailed information about the public rabbitmq-fips Chainguard Image."
date: 2024-02-29 16:25:55
lastmod: 2024-02-29 16:25:55
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
weight: 550
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=false url="/chainguard/chainguard-images/reference/rabbitmq-fips/" >}}
{{< tab title="Details" active=true url="/chainguard/chainguard-images/reference/rabbitmq-fips/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/rabbitmq-fips/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/rabbitmq-fips/provenance_info/" >}}
{{</ tabs >}}

This page shows detailed information about the Chainguard **rabbitmq-fips** Image.

|              | latest-dev                  | latest                      |
|--------------|-----------------------------|-----------------------------|
| Default User | `rabbitmq`                  | `rabbitmq`                  |
| Entrypoint   | `/usr/sbin/rabbitmq-server` | `/usr/sbin/rabbitmq-server` |
| CMD          | not specified               | not specified               |
| Workdir      | `/var/lib/rabbitmq`         | `/var/lib/rabbitmq`         |
| Has apk?     | yes                         | no                          |
| Has a shell? | yes                         | yes                         |

Check the [tags history page](/chainguard/chainguard-images/reference/rabbitmq-fips/tags_history/) for the full list of available tags.

## Packages Included
The table shows package distribution across variants.

|                               | latest-dev | latest |
|-------------------------------|------------|--------|
| `apk-tools`                   | X          |        |
| `bash`                        | X          | X      |
| `busybox`                     | X          | X      |
| `ca-certificates-bundle`      | X          | X      |
| `chainguard-baselayout`       | X          | X      |
| `erlang-fips-26`              | X          | X      |
| `git`                         | X          |        |
| `glibc`                       | X          | X      |
| `glibc-locale-en`             | X          | X      |
| `glibc-locale-posix`          | X          | X      |
| `ld-linux`                    | X          | X      |
| `libbrotlicommon1`            | X          |        |
| `libbrotlidec1`               | X          |        |
| `libcrypt1`                   | X          | X      |
| `libcrypto3`                  | X          | X      |
| `libcurl-openssl4`            | X          |        |
| `libexpat1`                   | X          |        |
| `libgcc`                      | X          | X      |
| `libidn2`                     | X          |        |
| `libnghttp2-14`               | X          |        |
| `libpcre2-8-0`                | X          |        |
| `libpsl`                      | X          |        |
| `libssl3`                     | X          |        |
| `libstdc++`                   | X          | X      |
| `libunistring`                | X          |        |
| `ncurses`                     | X          | X      |
| `ncurses-terminfo-base`       | X          | X      |
| `openssl-config-fipshardened` | X          | X      |
| `openssl-provider-fips`       | X          | X      |
| `rabbitmq-server-fips`        | X          | X      |
| `tzdata`                      | X          | X      |
| `wget`                        | X          |        |
| `wolfi-baselayout`            | X          | X      |
| `zlib`                        | X          | X      |

