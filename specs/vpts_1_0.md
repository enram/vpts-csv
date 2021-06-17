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

- The following fields are allowed in the CSV data:

| Name     	| Required 	| Description                        	                        | Type/format           |
|----------	|----------	|------------------------------------	                        |--------------------	|
| datetime 	| yes      	| Event date                         	                        | ISO8601 string     	|
| height   	| yes      	| Height above mean sea level, m       	                        | Positive Integer      |
| dens     	| yes      	| Density                            	                        | Positive float        |
| ff       	| yes      	| Horizontal speed, m/s                                         | Positive float        |
| dd       	| yes      	| Direction, degrees                   	                        | Positive float        |
| eta      	| yes      	| Linear reflectivity                	                        | Positive float        |
| sd_vvp   	| yes      	| Radial velocity standard deviation 	                        | Positive float        |
| DBZH     	| yes      	| Total reflectivity factor          	                        | Float              	|
| dbz      	| no       	| Animal reflectivity factor, dBZ                               | Float              	|
| u        	| no       	| Speed component west to east, m/s                             | Float              	|
| v        	| no       	| Speed component north to south, m/s                           | Float              	|
| gap      	| no       	| Angular data gap detected in                                  | Boolean              	|
| w        	| no       	| Vertical speed, m/s                                           | Float              	|
| n_dbz    	| no       	| Number of data points used for reflectivity-based estimates   | Integer               |
| n         | no        | Number of data points used for the speed estimates            | Positive Integer      |
| n_all     | no        | Number of data points used for sd_vvp                         | Positive Integer      |
| n_dbz_all | no        | Number of data points used for DBZH                           | Positive Integer      |

(TODO: make sure type/format have a clear datapackage-type mapping)

- CSV data rows are ordered: first by `datetime` then `height` columns.
- To make data exploration (by humans!) more user-friendly, it is considered good practice (but not mandatory) that the 
  field order (in CSV file) respect the field order in the table below.