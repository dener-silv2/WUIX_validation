# The WUIX index validation

## Overview

This repository contains a Python script for statistical analysis of WUIX (Wildland-Urban Interface Exposure) results. 
The script imports village parameters, merges WUIX results with building polygons, prepares visual distributions of the data, tests data normality, and applies statistical methods to assess differences between types of affectation.

* This work is part of the WUIX index testing campaign, and was presented originally in the **article: [Assessing the Accuracy of the Wildland–Urban Interface Index in Portuguese Rural Villages’ Context: A Case Study of the 2017 Pedrógão Grande Wildfire](https://doi.org/10.3390/fire7030090)**

## Usage

### Requirements

- Python 3.x
- Required Python packages listed in `scripts` &#8594; [`requirements.txt`](https://github.com/dener-silv2/WUIX_validation/blob/main/script/requirements.txt) 

### Instructions

1. Clone the repository:

```bash
git clone https://github.com/dener-silv2/WUIX_validation.git
```

2. Navigate to the repository directory:

```bash
cd .\WUIX_validation
```

3. Install required packages:

```bash
pip install -r .\scripts\requirements.txt
```

## The main script

> [**statistical_analysis.ipynb**](https://github.com/dener-silv2/WUIX_validation/blob/main/script/statistical_analysis.ipynb)


## Script Overview

The script performs the following steps:

&#10102;   **Import Village Parameters**: Loads village parameters from a JSON file.

&#10103;   **Merge WUIX Results with Building Polygons**: Converts ASCII files to raster TIFF files and then to shapefiles, merges the WUIX results with building polygons, and saves the results to a shapefile.

&#10104;   **Join Villages and Prepare Visuals**: Imports data from different villages, and prepares visuals showing the data distribution.

&#10105;   **Test the Normality of the Data**: Tests the normality of the data using the Shapiro-Wilk test and Kolmogorov-Smirnov test.

&#10106;   **Assumption of Non-Normally Distributed Data**: Performs statistical tests such as Kruskal-Wallis and Dunn's test assuming non-normally distributed data.

&#10107;   **Correlation of Real Case and WUIX by N_number**: Calculates correlations using Spearman's rank correlation coefficient.

&#10148;   **Assumption of normally and Correlation**: Even though the data was not normal, it performs statistical tests such as ANOVA and Tukey's test assuming normally distributed data and calculates correlations using Pearson's correlation coefficient for evetual different data.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details.

## Acknowledgments and funding

>  This work was financed by National Funds through the Portuguese funding agency, FCT - Fundação para a Ciência e a Tecnologia, within the project INHAVIT, reference MTS/BRB/0086/2020.
