---
title: "Image Overview: k8s-sidecar-fips"
linktitle: "k8s-sidecar-fips"
type: "article"
layout: "single"
description: "Overview: k8s-sidecar-fips Chainguard Image"
date: 2024-02-29 16:25:55
lastmod: 2024-02-29 16:25:55
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
menu: 
  docs: 
    parent: "images-reference"
weight: 500
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=true url="/chainguard/chainguard-images/reference/k8s-sidecar-fips/" >}}
{{< tab title="Details" active=false url="/chainguard/chainguard-images/reference/k8s-sidecar-fips/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/k8s-sidecar-fips/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/k8s-sidecar-fips/provenance_info/" >}}
{{</ tabs >}}



<!--overview:start-->
Minimal image with the k8s-sidecar app. **EXPERIMENTAL**
<!--overview:end-->

<!--getting:start-->
## Download this Image
The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/k8s-sidecar:latest
```
<!--getting:end-->

<!--body:start-->
## Using k8s-sidecar

The Chainguard k8s-sidecar image contains the k8s-sidecar python app.
The default entrypoint just runs the `k8s-sidecar` app without any flags.

This image is a drop-in replacement for the upstream image.
For full documentation on how to configure the app, check the [upstream documentation](https://github.com/kiwigrid/k8s-sidecar).

```shell
$ docker run cgr.dev/chainguard/k8s-sidecar
{"time": "2023-03-31T11:50:30.950603+00:00", "msg": "Starting collector", "level": "INFO"}
{"time": "2023-03-31T11:50:30.950708+00:00", "msg": "No folder annotation was provided, defaulting to k8s-sidecar-target-directory", "level": "WARNING"}
{"time": "2023-03-31T11:50:30.950751+00:00", "msg": "Should have added {LABEL} as environment variable! Exit", "level": "CRITICAL"}
```
<!--body:end-->

