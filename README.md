# Harmonie.jl

[![Build Status](https://travis-ci.com/hirlam/Harmonie.jl.svg?branch=master)](https://travis-ci.com/hirlam/Harmonie.jl)
[![Coverage Status](https://coveralls.io/repos/github/Hirlam/Harmonie.jl/badge.svg?branch=master)](https://coveralls.io/github/Hirlam/Harmonie.jl?branch=master)

[json-schema](https://json-schema.org/) validation of [Harmonie](http://hirlam.org/) configuration files 

## Install

Harmonie.jl is in the [HarmonieRegistry](https://github.com/Hirlam/HarmonieRegistry) and can be installed with (Hit `]` in the Julia REPL to go into package mode)  

```julia  
(v1.7) pkg> add Harmonie 
```

## Roadmap 
Aim is that in the future this repository will handle everything related to "configuration" in the Harmonie scripting system. Unit tests will validate that for each (ecflow) task the "input files" are created  correctly (namelist, symbolic links to initial conditions, etc.  (roughly speaking for each script it should create the content of WDIR)). This would allow changes to the scripting system to be validated without having to run the full current Harmonie testbed. (The testbed will still be needed for changes to the Fortran code and as an integration test of the whole system). For this creation of namelist and setting up of symbolic links that is currently done in the scripts would have to "externalized" and moved to this repository. The scripts in the Harmonie repository will only call Fortran binaries. The perl code in the current Harmonie scripting should be translated and moved to this repository. 

## Open issues 
- handling of  EPS configuration 

## to do
- Add schema for all namelists
- Add schema for param_bator.cfg, LISTE_NOIRE_DIAP, etc.
- Add schema for codetype obstype from the ECMWF odb json files.
- Add schema for submit.ecgb-cca submit.LinuxPC etc.
- Add schema for submission.db information
- Add schema fro build configuration including compiler options
- Add schema for selection mechanism for VarBC predictors
- Add schema for MARS request files
- Add schema for ECMWF cycles. This should allow e.g. to validate BDINT etc. better. Also it should warn if ECMWF cycles changes during the time range (DTGBEG DTGEND). 
- Add schema for ecflow  tasks/families (document input output, such that the graphviz figure can be generated automatically)` 
- Add schema for harmonie testbed (Harmonie_configurations.pm Harmonie_testbed.pl)



Check https://www.commonwl.org/

