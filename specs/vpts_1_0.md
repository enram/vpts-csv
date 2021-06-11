# vpts 1.0 specifications

**TODO: complete and polish this document**

A vpts data package is a fully compliant `Tabular data package` 
(a subset of [Frictionless Data Package](https://frictionlessdata.io/data-package/)), that also conforms to the 
specifications below:

- It contains 2 files: a single CSV data file and metadata (in `datapackage.json`)
- This CSV file contains data (bird profiles) covering **a single weather radar** over an **arbitrary 
  period of time** and **one or** (more typically) **several heights**.
- Information (metadata) about the **weather radar**, the **temporal range** and the **available heights** are expressed
  in `datapackage.json` TODO: say how (for temporal resolution it'll be an integer representing the number of seconds, not considering gaps)
- The temporal range must be expressed as 
  
```
"temporal": {
    "start": "2019-10-15T14:30:00Z", // ISO8601
    "end": "2019-10-15T23:55:00Z" // ISO8601
  }
```
as a top-level element of datapackage.json

- Temporal gaps may happen
  
- The following fields are allowed in the CSV data:
   - `datetime` (ISO8601)
   - `height` (integer, in meters, above sea level) 
   - `...`
TODO: complete list, indicate which ones are mandatory
TODO: say that it's better (for human consumption) but not mandatory to have files in a specific order     

- CSV rows are ordered: first by `datetime` then `height` columns.  