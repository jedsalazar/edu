---
title: "Network Requirements"
linktitle: "Network Requirements"
lead: "Using Chainguard Images and Enforce with firewalls, access control lists, and proxies"
type: "article"
description: "Using Chainguard Images and Enforce with firewalls, access control lists, and proxies"
date: 2023-09-08T08:49:31+00:00
lastmod: 2023-11-29T15:22:20+01:00
draft: false
aliases:
  - /chainguard/chainguard-images/reference/network-requirements/
  - /chainguard/chainguard-enforce/reference/network-requirements/
tags: ["Chainguard Images", "Chainguard Enforce", "Product", "Reference"]
images: []
toc: true
weight: 001
---

This document provides an overview of network requirements for using [Chainguard Images](https://www.chainguard.dev/chainguard-images?utm_source=docs). To use Chainguard tools and Images in environments with firewalls, VPNs, and IDS/IPS systems, you will need to add some rules to allow traffic into and out of your networks.

## Chainguard Images Hosts

This table lists the DNS hostnames, associated ports, and protocols that will need to be allowed through firewalls and proxies to use Chainguard Images:

| Hostname                | Port | Protocol | Notes                                 |
| ----------------------- | ---- | -------- | ------------------------------------- |
| cgr.dev                 | 443  | HTTPS    | Main image registry                   |
| console.enforce.dev     | 443  | HTTPS    | Chainguard dashboard                  |
| console-api.enforce.dev | 443  | HTTPS    | Registry API endpoint                 |
| enforce.dev             | 443  | HTTPS    | Registry authentication               |
| dl.enforce.dev          | 443  | HTTPS    | `chainctl` downloads                  |
| issuer.enforce.dev      | 443  | HTTPS    | Registry STS (Security Token Service) |
| packages.wolfi.dev      | 443  | HTTPS    | Package repository                    |

Note that to be able to authenticate with Chainguard systems, you will need to ensure access to and from the following CIDR ranges:

{{< blurb/enforce-ips >}}

## Chainguard Images Third-party Hosts

This table lists the third-party DNS hostnames, associated ports, and protocols that will need to be allowed through firewalls and proxies to use Chainguard Images:

| Hostname                                                  | Port | Protocol | Notes                        |
| --------------------------------------------------------- | ---- | -------- | ---------------------------- |
| ghcr.io                                                   | 443  | HTTPS    | Used for wolfi development   |
| \*.r2.cloudflarestorage.com                               | 443  | HTTPS    | Blob storage for cgr.dev     |
| 9236a389bd48b984df91adc1bc924620.r2.cloudflarestorage.com | 443  | HTTPS    | Blob storage for cgr.dev     |
| chainguardhelp.zendesk.com                                | 443  | HTTPS    | Support access for customers |
| storage.googleapis.com                                    | 443  | HTTPS    | `chainctl` downloads         |

You can use either the single `9236a389bd48b984df91adc1bc924620.r2.cloudflarestorage.com` host or the wildcard `*.rc.cloudflarestorage.com` hostname in your firewall and proxy configurations. However, the `9236a389bd48b984df91adc1bc924620.r2.cloudflarestorage.com` hostname may change at some point in the future.

## Ingress and Egress

Connections to the hosts listed on this page are generally initiated as new outbound connections. If you are using stateful firewall rules, then you will need to add symmetric rules to ensure that traffic flows correctly.

You will need egress rules that allow new traffic to the hosts listed here. You will need corresponding ingress rules that allow related and established traffic.

For the CIDR ranges listed here, ensure that you allow incoming connections from those networks. These IPs are used for workload discovery on public clouds.

## DNS Records and TTLs

Many of the hosts listed on this page use multiple DNS A records or CNAME aliases. Additionally, many A records have a short time to live of 60 seconds, and the majority are less than an hour (3600s).

If your network filters traffic based on IP addresses, ensure that any firewalls update their rules at an appropriate interval to match the TTL for each DNS record.
