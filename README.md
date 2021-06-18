---
permalink: /
---

# Time series of vertical profiles of biological signals (vpts)

**VPTS** is a community developed **data exchange format** for biological signals detected by weather radars. VPTS data are time series of vertical profiles of biological signals. These express the density, speed and direction of birds, bats and insects within the weather radar volume, grouped in altitude layers. A VPTS is a [Frictionless Data Package](https://specs.frictionlessdata.io/data-package/) that consists of:

File | Description
--- | ---
`datapackage.json` | [Metadata](https://enram.github.io/vpts/metadata/) regarding the data package.
`vpts.csv` | Table with [vpts data](https://enram.github.io/vpts/data).

Status: under heavy development, **not usable yet**

## Goal for v1.0

Create end-to-end working proof of concept:

1. Bird profiles are generated with [vol2bird](https://github.com/adokter/vol2bird/)
2. They are aggregated to a single **vpts** with [vph5_to_vpts](https://github.com/enram/vptstools)
3. The resulting **vpts** can be consumed and visualized by [CROW](https://github.com/inbo/crow)

## Contribute

Want to get involved in the development of VPTS? Watch [the repository](https://github.com/enram/vpts) to get notifications and participate in [issue discussions](https://github.com/enram/vpts/issues).
