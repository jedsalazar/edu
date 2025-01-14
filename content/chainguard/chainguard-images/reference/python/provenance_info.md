---
title: "Provenance Information for python Images"
type: "article"
unlisted: true
description: "Provenance information for python Chainguard Image"
date: 2022-11-01T11:07:52+02:00
lastmod: 2024-03-01 12:14:22
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
weight: 600
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=false url="/chainguard/chainguard-images/reference/python/" >}}
{{< tab title="Details" active=false url="/chainguard/chainguard-images/reference/python/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/python/tags_history/" >}}
{{< tab title="Provenance" active=true url="/chainguard/chainguard-images/reference/python/provenance_info/" >}}
{{</ tabs >}}

All Chainguard Images contain verifiable signatures and high-quality SBOMs (software bill of materials), features that enable users to confirm the origin of each image build and have a detailed list of everything that is packed within.

You'll need [cosign](https://docs.sigstore.dev/cosign/overview/) and [jq](https://stedolan.github.io/jq/) in order to download and verify image attestations.

### Registry and Tags for python Image
Attestations are provided per image build, so you'll need to specify the correct tag and registry when pulling attestations from an image with `cosign`.

| Registry                     | Tags                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cgr.dev/chainguard`         | latest, latest-dev                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| `cgr.dev/chainguard-private` | 3, 3-dev, 3-fips, 3-fips-dev, 3.10, 3.10-dev, 3.10-fips, 3.10-fips-dev, 3.10.11, 3.10.11-dev, 3.10.12, 3.10.12-dev, 3.10.12-fips, 3.10.12-fips-dev, 3.10.12-r0-fips, 3.10.12-r0-fips-dev, 3.10.13, 3.10.13-dev, 3.10.13-fips, 3.10.13-fips-dev, 3.10.13-r0-fips, 3.10.13-r0-fips-dev, 3.10.13-r1-fips, 3.10.13-r1-fips-dev, 3.11, 3.11-dev, 3.11-fips, 3.11-fips-dev, 3.11.3, 3.11.3-dev, 3.11.4, 3.11.4-dev, 3.11.4-fips, 3.11.4-fips-dev, 3.11.4-r0-fips, 3.11.4-r0-fips-dev, 3.11.5, 3.11.5-dev, 3.11.5-fips, 3.11.5-fips-dev, 3.11.5-r0-fips, 3.11.5-r0-fips-dev, 3.11.5-r1-fips, 3.11.5-r1-fips-dev, 3.11.5-r2-fips, 3.11.5-r2-fips-dev, 3.11.6, 3.11.6-dev, 3.11.6-fips, 3.11.6-fips-dev, 3.11.6-r0-fips, 3.11.6-r0-fips-dev, 3.11.7, 3.11.7-dev, 3.11.8, 3.11.8-dev, 3.12, 3.12-dev, 3.12.0, 3.12.0-dev, 3.12.1, 3.12.1-dev, 3.12.2, 3.12.2-dev, 3.7, 3.7.16, 3.7.17, 3.8, 3.8-dev, 3.8-dev-dev, 3.8.10, 3.8.10-dev, 3.8.16, 3.8.16-dev, 3.8.17, 3.8.17-dev, 3.8.18, 3.8.18-dev, 3.9, 3.9-dev, 3.9-dev-dev, 3.9.16, 3.9.16-dev, 3.9.17, 3.9.17-dev, 3.9.18, 3.9.18-dev, latest, latest-dev, latest-fips, latest-fips-dev |


- `cgr.dev/chainguard` - the Public Registry contains our **Developer Images**, which typically comprise the `latest*` versions of an image.
- `cgr.dev/chainguard-private` - the Private/Dedicated Registry contains our **Production Images**, which include all versioned tags of an image and special images that are not available in the public registry (including FIPS images and other custom builds).

The commands listed on this page will default to the `latest` tag, but you can specify a different tag to fetch attestations for.

## Verifying python Image Signatures
The **python** Chainguard Images are signed using Sigstore, and you can check the included signatures using `cosign`.

The `cosign verify` command will pull detailed information about all signatures found for the provided image.

### Public Registry

```shell
cosign verify \
  --certificate-oidc-issuer=https://token.actions.githubusercontent.com \
  --certificate-identity=https://github.com/chainguard-images/images/.github/workflows/release.yaml@refs/heads/main \
  cgr.dev/chainguard/python | jq
```

### Private/Dedicated Registry

```shell
cosign verify \
--certificate-oidc-issuer=https://token.actions.githubusercontent.com \
--certificate-identity=https://github.com/chainguard-images/images-private/.github/workflows/release.yaml@refs/heads/main \
cgr.dev/chainguard-private/python | jq
```

## Downloading python Image Attestations

The following [attestations](https://slsa.dev/attestation-model) for the python image can be obtained and verified via cosign:

| Attestation Type | Description |
|----------------|-------------|
| `https://slsa.dev/provenance/v1` | The [SLSA 1.0](https://slsa.dev/spec/v1.0/provenance) provenance attestation contains information about the image build environment. |
| `https://apko.dev/image-configuration` | Contains the configuration used by that particular image build, including direct dependencies, user accounts, and entry point. |
| `https://spdx.dev/Document` | Contains the image SBOM (Software Bill of Materials) in SPDX format. |


To download an attestation, use the `cosign download attestation` command and provide both the predicate type and the build platform. For example, the following command will obtain the SBOM for the python image on `linux/amd64`:

### Public Registry

```shell
cosign download attestation \
  --platform=linux/amd64 \
  --predicate-type=https://spdx.dev/Document \
  cgr.dev/chainguard/python | jq -r .payload | base64 -d | jq .predicate
```

### Private/Dedicated Registry

```shell
cosign download attestation \
--platform=linux/amd64 \
--predicate-type=https://spdx.dev/Document \
cgr.dev/chainguard-private/python | jq -r .payload | base64 -d | jq .predicate
```

By default, this command will fetch the SBOM assigned to the `latest` tag. You can also specify the tag you want to fetch the attestation from.

To download a different attestation, replace the `--predicate-type` parameter value with the desired attestation URL identifier.

## Verifying python Image Attestations
You can use the `cosign verify-attestation` command to check the signatures of the python image attestations:

### Public Registry

```shell
cosign verify-attestation \
  --type https://spdx.dev/Document \
  --certificate-oidc-issuer=https://token.actions.githubusercontent.com \
  --certificate-identity=https://github.com/chainguard-images/images/.github/workflows/release.yaml@refs/heads/main \
  cgr.dev/chainguard/python
```

### Private/Dedicated Registry

```shell
cosign verify-attestation \
--type https://spdx.dev/Document \
--certificate-oidc-issuer=https://token.actions.githubusercontent.com \
--certificate-identity=https://github.com/chainguard-images/images-private/.github/workflows/release.yaml@refs/heads/main \
cgr.dev/chainguard-private/python
```

This will pull in the signature for the attestation specified by the `--type` parameter, which in this case is the SPDX attestation. You will receive output that verifies the SBOM attestation signature in cosign's transparency log:

```
Verification for cgr.dev/chainguard/python --
The following checks were performed on each of these signatures:
- The cosign claims were validated
- Existence of the claims in the transparency log was verified offline
- The code-signing certificate was verified using trusted certificate authority certificates
Certificate subject:  https://github.com/chainguard-images/images/.github/workflows/release.yaml@refs/heads/main
Certificate issuer URL:  https://token.actions.githubusercontent.com
GitHub Workflow Trigger: schedule
GitHub Workflow SHA: da283c26829d46c2d2883de5ff98bee672428696
GitHub Workflow Name: .github/workflows/release.yaml
GitHub Workflow Trigger chainguard-images/images
GitHub Workflow Ref: refs/heads/main
...
```
