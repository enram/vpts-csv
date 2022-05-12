---
layout: home
title: VPTS
description: Data exchange format for biological signals detected by weather radars
permalink: /
---

[![Project Status: WIP](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip)

VPTS is a community developed **data exchange format** for biological signals detected by weather radars. VPTS (vertical profile time series) express the density, speed and direction of biological signals such as birds, bats and insects within a weather radar volume, grouped into altitude layers and measured over time.

[Description of the format]({{ '/format/' | relative_url }})

## Goal for v1.0

Create end-to-end working proof of concept:

1. Bird profiles are generated with [vol2bird](https://github.com/adokter/vol2bird/).
2. They are aggregated to a single **VPTS** with [vph5_to_vpts](https://github.com/enram/vptstools).
3. The resulting **VPTS** can be consumed and visualized by [CROW](https://github.com/inbo/crow) and [bioRad](https://github.com/adokter/bioRad).

## Contribute

Questions? Suggestions? Contribute to the development of VPTS by watching the [repository](https://github.com/enram/vpts) and participating in [issue discussions](https://github.com/enram/vpts/issues).
