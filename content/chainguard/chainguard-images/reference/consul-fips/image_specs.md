---
title: "consul-fips Image Details"
type: "article"
unlisted: true
description: "Detailed information about the public consul-fips Chainguard Image."
date: 2024-02-29 16:25:55
lastmod: 2024-02-29 16:25:55
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
weight: 550
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=false url="/chainguard/chainguard-images/reference/consul-fips/" >}}
{{< tab title="Details" active=true url="/chainguard/chainguard-images/reference/consul-fips/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/consul-fips/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/consul-fips/provenance_info/" >}}
{{</ tabs >}}

This page shows detailed information about the Chainguard **consul-fips** Image.

|              | latest-dev                      | latest                          |
|--------------|---------------------------------|---------------------------------|
| Default User | `root`                          | `root`                          |
| Entrypoint   | `/usr/bin/docker-entrypoint.sh` | `/usr/bin/docker-entrypoint.sh` |
| CMD          | `agent -dev -client 0.0.0.0`    | `agent -dev -client 0.0.0.0`    |
| Workdir      | not specified                   | not specified                   |
| Has apk?     | yes                             | no                              |
| Has a shell? | yes                             | yes                             |

Check the [tags history page](/chainguard/chainguard-images/reference/consul-fips/tags_history/) for the full list of available tags.

## Packages Included
The table shows package distribution across variants.

|                                          | latest-dev | latest |
|------------------------------------------|------------|--------|
| `apk-tools`                              | X          |        |
| `bash`                                   | X          |        |
| `busybox`                                | X          | X      |
| `ca-certificates-bundle`                 | X          | X      |
| `chainguard-baselayout`                  | X          | X      |
| `consul-1.17-fips`                       | X          | X      |
| `consul-1.17-fips-oci-entrypoint`        | X          | X      |
| `consul-1.17-fips-oci-entrypoint-compat` | X          | X      |
| `curl`                                   | X          | X      |
| `dumb-init`                              | X          | X      |
| `git`                                    | X          |        |
| `glibc`                                  | X          | X      |
| `glibc-locale-posix`                     | X          | X      |
| `ld-linux`                               | X          | X      |
| `libbrotlicommon1`                       | X          | X      |
| `libbrotlidec1`                          | X          | X      |
| `libcap`                                 | X          | X      |
| `libcap-utils`                           | X          | X      |
| `libcrypt1`                              | X          | X      |
| `libcrypto3`                             | X          | X      |
| `libcurl-openssl4`                       | X          | X      |
| `libexpat1`                              | X          |        |
| `libidn2`                                | X          | X      |
| `libnghttp2-14`                          | X          | X      |
| `libpcre2-8-0`                           | X          |        |
| `libpsl`                                 | X          | X      |
| `libssl3`                                | X          | X      |
| `libunistring`                           | X          | X      |
| `ncurses`                                | X          |        |
| `ncurses-terminfo-base`                  | X          |        |
| `openssl-config-fipshardened`            | X          | X      |
| `openssl-provider-fips`                  | X          | X      |
| `su-exec`                                | X          | X      |
| `wget`                                   | X          |        |
| `wolfi-baselayout`                       | X          | X      |
| `zlib`                                   | X          | X      |

