# ebsa

This repository hosts R code to generate shapefiles of biodiversity indices and other metrics based on OBIS data in support of the CBD EBSA process. The current version of the code uses a CSV export of the relevant OBIS fields, and exports shapefiles as well as map images. Core functionality can be found in `lib.R`, overall metrics are calculated in `script.R`, and metrics for data subsets are calculated in `subsets.R`.

![maps](metrics.png)

## setup

```bash
# install system dependencies
apt install libgsl-dev

# install devtools if needed
Rscript -e 'if (!requireNamespace("devtools")) install.packages("devtools")'

# install global Imports from DESCRIPTION
Rscript -e 'devtools::install(pkg=".", quick=TRUE, upgrade=TRUE)'
```

* Tested w/ R v3.6.1 on ubuntu 16.04
* Requires R > v3.5.0 (bc cowplot)


# usage
```bash
Rscript ./script
```
