# vpts 1.0 specifications

**TODO: complete and polish this document**

A vpts data package is a fully compliant `Tabular data package` 
(a subset of [Frictionless Data Package](https://frictionlessdata.io/data-package/)), that contains bird profile data 
(covering **a single weather radar** over an **arbitrary period of time** and **one or** (more typically) **several heights**)
and that also conforms to the specifications below:

- It contains 2 files: 
  - The data itself (bird profiles) in a CSV file  
  - Metadata in `datapackage.json`
  
## Metadata (`datapackage.json`)
- Since a vpts data package is a valid data package, `datapackage.json` must follow the
  [the descriptor specifications](https://dataprotocols.org/data-packages/#descriptor-datapackagejson), with the following 
  additional constraints:
- Information (metadata) about the **weather radar**, the **temporal range** and the **available heights** are expressed
  in `datapackage.json` TODO: say how (for temporal resolution it'll be an integer representing the number of seconds, not considering gaps)
- The temporal range must be expressed as a top-level element of datapackage.json:
  
```
"temporal": {
    "start": "2019-10-15T14:30:00Z", // ISO8601
    "end": "2019-10-15T23:55:00Z" // ISO8601
  }
```
- Temporal gaps may happen
  
(to be continued)
  
## Data file (bird profiles)

To avoid duplication:

- all column information moved to `vpts-able-schema.json`
- table-wide specs moved to `pages/data.md`
