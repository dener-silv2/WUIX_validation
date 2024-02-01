# The WUIX index validation

## Overview

This repository contains a Python script for statistical analysis of WUIX (Wildland-Urban Interface Exposure) results. 
The script imports village parameters, merges WUIX results with building polygons, prepares visual distributions of the data, tests data normality, and applies statistical methods to assess differences between types of affectation.

* This work is part of the WUIX index testing campaign, and was presented originally in the **article "TOFILL"**

## Usage

### Requirements

- Python 3.x
- Required Python packages listed in `requirements.txt`

### Instructions

1. Clone the repository:

```bash
git clone https://github.com/dener-silv2/WUIX_validation.git
```

2. Navigate to the repository directory:

```bash
cd your_repository
```

3. Install required packages:

```bash
pip install -r requirements.txt
```

## The script main script

- statistical_analysis.ipynb


## Script Overview

The script performs the following steps:

1. **Import Village Parameters**: Loads village parameters from a JSON file.

2. **Merge WUIX Results with Building Polygons**: Converts ASCII files to raster TIFF files and then to shapefiles, merges the WUIX results with building polygons, and saves the results to a shapefile.

3. **Join Villages and Prepare Visuals**: Imports data from different villages, and prepares visuals showing the data distribution.

4. **Test the Normality of the Data**: Tests the normality of the data using the Shapiro-Wilk test and Kolmogorov-Smirnov test.

5. **Assumption of Non-Normally Distributed Data**: Performs statistical tests such as Kruskal-Wallis and Dunn's test assuming non-normally distributed data.

6. **Correlation of Real Case and WUIX by N_number**: Calculates correlations using Spearman's rank correlation coefficient.

X. **Assumption of normally and Correlation**: Even though the data was not normal, it performs statistical tests such as ANOVA and Tukey's test assuming normally distributed data and calculates correlations using Pearson's correlation coefficient for evetual different data.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

'''- [Original Dataset Source](https://example.com)'''
