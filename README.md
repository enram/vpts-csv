# vpts

vpts is a community developed data exchange format for time series of vertical profiles (vpts).

It is a specialized kind of [Frictionless Data Package](https://frictionlessdata.io/data-package/).

Status: under heavy development, **not usable yet**

Discussions should take place into issues, each subsequent decision **must** be reflected in [the specification document](specs/vpts_1_0.md).

## Goals of version 1.0

- First usable, stable version
- Heavily inspired by the [vol2bird](https://github.com/adokter/vol2bird/) CSV output  
- End-to-end working proof of concept:   
    1) bird profiles are generated with [vol2bird](https://github.com/adokter/vol2bird/)
    2) they are aggregated to a single **vpts** with [vph5_to_vpts](https://github.com/enram/vptstools)
    3) The resulting **vpts** can be consumed and visualized by [CROW](https://github.com/inbo/crow)
    
## Specifications of version 1.0

See [vpts_1_0.md](specs/vpts_1_0.md).

## Further goals

- Better adapted to data originating from other tools/formats than vol2bird (CAJUN, ...)
- Fix youthful errors and early misjudgements