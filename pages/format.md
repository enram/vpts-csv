---
layout: tables
title: Format
description: Description of the VPTS format and fields
permalink: /format/
---

VPTS is a tabular format (rows and columns), allowing data to be exchanged as CSV files. Rows express the density, speed and direction of biological signals such as birds, bats and insects within the weather radar volume, grouped into altitude layers (`height`) and measured over time (`datetime`). Columns/fields are defined below.

## Example

```
radar,datetime,height,u,v,w,ff,dd,sd_vvp,gap,eta,dens,dbz,dbz_all,n,n_dbz,n_all,n_dbz_all,rcs,sd_vvp_threshold,vcp,radar_longitude,radar_latitude,radar_height,radar_wavelength
KBGM,2016-09-01T00:02:00Z,0,,,,,,,TRUE,,,,,0,0,0,0,11,2,,-75.98472,42.19972,519,10.6
KBGM,2016-09-01T00:02:00Z,200,,,,,,,TRUE,,,,,0,0,0,0,11,2,,-75.98472,42.19972,519,10.6
KBGM,2016-09-01T00:02:00Z,400,,,,,,2.81,TRUE,30.8,2.8000000000000003,1.54,3.77,326,356,22485,28416,11,2,,-75.98472,42.19972,519,10.6
KBGM,2016-09-01T00:02:00Z,600,4.14,3.84,12.17,5.65,47.2,2.8,FALSE,46.9,4.263636363636364,3.36,0.5,9006,13442,65947,104455,11,2,,-75.98472,42.19972,519,10.6
```

## Requirements

- Data MUST[^1] include the names of the fields (e.g. as a header row).
- Data MUST refer to fields using the names defined below.
- Data MUST at least include the required fields (indicated with `*` below).
- Required fields (indicated with `*` below) SHOULD NOT be empty.
- Field values SHOULD match the data types as defined below.
- Field values SHOULD meet the constraints as defined below (e.g. `minimum`).
- Data SHOULD be ordered by `datetime` and `height` within a `radar`.
- Data SHOULD have a constant number of `height` records for all `datetime`s of a `radar`.
- It is RECOMMENDED to organize the fields in the order presented below.

[^1]: The key words `MUST`, `MUST NOT`, `REQUIRED`, `SHALL`, `SHALL NOT`, `SHOULD`, `SHOULD NOT`, `RECOMMENDED`, `MAY`, and `OPTIONAL` in this document are to be interpreted as described in [RFC 2119](https://www.ietf.org/rfc/rfc2119.txt).
