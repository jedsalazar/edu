---
title: "karpenter Image Tags History"
type: "article"
unlisted: true
description: "Image Tags and History for the karpenter Chainguard Image"
date: 2023-06-22T11:07:52+02:00
lastmod: 2024-03-01 12:14:22
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
weight: 700
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=false url="/chainguard/chainguard-images/reference/karpenter/" >}}
{{< tab title="Details" active=false url="/chainguard/chainguard-images/reference/karpenter/image_specs/" >}}
{{< tab title="Tags History" active=true url="/chainguard/chainguard-images/reference/karpenter/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/karpenter/provenance_info/" >}}
{{</ tabs >}}

The following tables contains the most recent tags and digests that can be used to pin your Dockerfile to a specific build of this image. Check our guide on [Using the Tag History API](/chainguard/chainguard-images/using-the-tag-history-api/) for information on how to fetch all tags from an image and how to pin your Dockerfile to a specific digest.

Please note that digests and timestamps only change when there is a change to the image, even though images are rebuilt every night. The "Last Changed" column indicates when the image was last modified, and doesn't always reflect the latest build timestamp. For more information about how our reproducible builds work, please refer to [this blog post](https://www.chainguard.dev/unchained/reproducing-chainguards-reproducible-image-builds).

### Public Registry
The Public Registry contains our **Developer Images**, which typically comprise the `latest*` versions of an image.

| Tag (s)       | Last Changed  | Digest                                                                    |
|---------------|---------------|---------------------------------------------------------------------------|
|  `latest`     | February 27th | `sha256:da43d265e2be7afc646ba02296c30a0c3b1210a68a22f626af9501541c009cbb` |
|  `latest-dev` | February 27th | `sha256:e371c9d4a11bb3314932364cedc9fb72b141602f87e023c2a1630ec54f58a608` |


### Private/Dedicated Registry
The Private/Dedicated Registry contains our **Production Images**, which include all versioned tags of an image and special images that are not available in the public registry (including FIPS images and other custom builds).

| Tag (s)                                       | Last Changed  | Digest                                                                    |
|-----------------------------------------------|---------------|---------------------------------------------------------------------------|
|  `latest` `0.34` `0.34.1` `0`                 | February 26th | `sha256:825d24feda8cac13f08fc41114b873f8a42b46b3037eabeb39f0de8a6ab20e08` |
|  `0.34-dev` `0.34.1-dev` `0-dev` `latest-dev` | February 26th | `sha256:ea6f1b7b07c884e7be07c3a93c716465b8220fbe2bf84a7f49cc1bf440c35865` |
|  `0.34.0-dev`                                 | February 17th | `sha256:bc792a458800ee813131a0f93d7621e8a6bd926b5a28fe296e502d5b23b22480` |
|  `0.34.0`                                     | February 6th  | `sha256:ead36acc490da8230b5437207bd82da9ac4cb8b2811ed0ed2aa9f6452a6fb1c9` |
|  `0.33-dev` `0.33.2-dev`                      | February 6th  | `sha256:9c224a4c22ea3e260dff1ea36f4905efd62b700597c7da724df3c33c9ef79a1a` |
|  `0.33.2` `0.33`                              | February 5th  | `sha256:56f63f201c6374e70bc8c847c0524d7bec4fe3fd91c0f19738b8bbda0801002e` |

