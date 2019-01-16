---
output: github_document
---

[![Build Status](https://travis-ci.org/eribul/coder.svg?branch=master)](https://travis-ci.org/eribul/coder)
[![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/eribul/coder?branch=master&svg=true)](https://ci.appveyor.com/project/eribul/coder)
[![codecov](https://codecov.io/gh/eribul/coder/branch/master/graph/badge.svg)](https://codecov.io/gh/eribul/coder)
[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)


<!-- README.md is generated from README.Rmd. Please edit that file --> 


# coder 

The goal of `coder` is to classify items from one dataset, using codes from a secondary source. 
Please se vigtnettes with introductionary examples! 

## Installation

You can (soon) install the released version of coder from [CRAN](https://CRAN.R-project.org) with:

``` r
# install.packages("coder") # Not yet!
```

And the development version from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("eribul/coder")
```

## Classification schemes

Classification schemes are used to classify items. 
These schemas are constructed by regular expressions for computational speed, 
but their content can be summarized and visualized for clarity.

The package includes several default classification schemes (so called `classcodes` objects).
Most of these are related to medical patient data (for classification of comorbidity and adverse events).

Arbitrary `classcodes` objects can be specified by the user. 

### Default classcodes


|clascodes                    |description                                                            |coding     |indices                                                                      |  N|     n|
|:----------------------------|:----------------------------------------------------------------------|:----------|:----------------------------------------------------------------------------|--:|-----:|
|charlson_icd10               |Comorbidity based on charlson                                          |icd10      |regex_rcs, charlson, deyo_ramano, dhoore, ghali, quan_original, quan_updated | 17|  1178|
|cps_icd10                    |comorbidity-polypharmacy score (CPS)                                   |icd10      |only_ordinary                                                                |  2| 12406|
|elix_icd10                   |Comorbidity based on elix                                              |icd10      |sum_all, sum_all_ahrq, walraven, sid29, sid30, ahrq_mort, ahrq_readm         | 31|  1517|
|ex_carbrands                 |Example data of car brand names and their producers.                   |ex_allcars |                                                                             |  7|    22|
|hip_adverse_events_icd10     |Adverse events after hip arthroplasty                                  |icd10      |                                                                             |  6|   306|
|hip_adverse_events_icd10_old |Adverse events after hip arthroplasty                                  |icd10      |sos, shar                                                                    |  3|   523|
|hip_fracture_ae_icd10        |Adverse events after hip arthroplasty                                  |icd10      |                                                                             |  1|   749|
|hip_fracture_ae_kva          |Adverse events after hip arthroplasty                                  |kva        |                                                                             |  1|   143|
|knee_adverse_events_icd10    |Adverse events after knee arthroplasty                                 |icd10      |                                                                             |  6|   278|
|rxriskv_atc                  |Comorbidity index 'RxRiskV'                                            |atc        |                                                                             | 39|  1170|
|rxriskv_modified_atc         |Comorbidity index 'RxRiskV' (unofficial modification by Anne Garland). |atc        |                                                                             | 42|  1391|

# Contribution

Contributions to this package are welcome. The preferred method of contribution is through a github pull request. Feel free to contact me by creating an issue. Please note that this project is released with a [Contributor Code of Conduct](CODE_OF_CONDUCT.md).
By participating in this project you agree to abide by its terms.
