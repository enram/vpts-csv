---
layout: tables
title: Format
description: Description of the VPTS format and fields
permalink: /format/
---

VPTS is a tabular format (rows and columns), allowing data to be exchanged as CSV files. Rows express the density, speed and direction of biological signals such as birds, bats and insects within the weather radar volume, grouped into altitude layers (`height`) and measured over time (`datetime`). Columns/fields are defined below.

- Data SHOULD contain all fields presented below.
- It is RECOMMENDED to organize fields in the order presented below.
- Fields indicated with `*` are REQUIRED (i.e. cannot be empty).
- Data MUST be ordered by `datetime` and `height` within a `radar`.

## Example

```
radar,datetime,height,u,v,w,ff,dd,sd_vvp,gap,eta,dens,dbz,dbz_all,n,n_dbz,n_all,n_dbz_all,rcs,sd_vvp_threshold,vcp,radar_lon,radar_lat,radar_height,radar_wavelength
KBGM,2016-09-01T00:02:00Z,0,,,,,,,TRUE,,,,,0,0,0,0,11,2,,-75.98472,42.19972,519,10.6
KBGM,2016-09-01T00:02:00Z,200,,,,,,,TRUE,,,,,0,0,0,0,11,2,,-75.98472,42.19972,519,10.6
KBGM,2016-09-01T00:02:00Z,400,,,,,,2.81,TRUE,30.8,2.8000000000000003,1.54,3.77,326,356,22485,28416,11,2,,-75.98472,42.19972,519,10.6
KBGM,2016-09-01T00:02:00Z,600,4.14,3.84,12.17,5.65,47.2,2.8,FALSE,46.9,4.263636363636364,3.36,0.5,9006,13442,65947,104455,11,2,,-75.98472,42.19972,519,10.6
```
