# Local Geary c in R

*Ali Syed* zasyed@uchicago.edu Geographical Sciences and Economics majors, College of the University of Chicago

*Sihan Mao* sihan@uchicago.edu Master in Public Policy Candidate, the University of Chicago Harris School of Public Policy

June 12, 2019

## Overview

R is well equipped with spatial operation tools. Spatial statistics, however, are not fully integrated into R environment. The objective of this project is to develop an R Notebook Tutorial to compute and visualize univariate local Geary c statistic. Success of this project would entail that the notebook tutorial is workable and effective enough to replicate the GeoDa local Geary c functions.

## Scope

The following scope describes the work to develop the local Geary c function in R. The team shall conduct research on: 

- the design of local Moran’s I and local Geary c<sup>1</sup>,
- localmoran.R script in **spdep** repository<sup>2</sup>,
- current available local Moran’s I tutorial in R<sup>3</sup>.


## Sample Data Description

**Dataset Description**: The dataset is the test dataset of tutorial for calculating local Geary c in R. The test requires a continuous variable as the attribute of polygons. The dataset includes Airbnb rents and boundaries of community areas in Chicago.

**Type**: Polygon shapefile; Observations: 77; Variables: 3 

**Variables to be included**: 

- *community* - name of community area 
- *AREAID* – ID number associated with community area 
- *price_pp* – price per person of Airbnb

**Data Table**:

<table>
  <tr>
    <td>Variable</td>
    <td>Type</td>
    <td>Example</td>
    <td>Source</td>
  </tr>
  <tr>
    <td><b>community<b></td>
    <td>string</td>
    <td><i>Kenwood<i></td>
    <td><a href="https://geodacenter.github.io/data-and-lab//airbnb_Chicago-2015">Chicago Data Portal</a></td>
  </tr>
  <tr>
    <td><b>AREAID<b></td>
    <td>int</td>
    <td><i>39<i></td>
    <td><a href="https://geodacenter.github.io/data-and-lab//airbnb_Chicago-2015">Chicago Data Portal</a></td>
  </tr>
      <tr>
    <td><b>price_pp<b></td>
    <td>double</td>
    <td><i>77.991453<i></td>
    <td><a href="http://insideairbnb.com/get-the-data.html">Inside Airbnb</a></td>
  </tr>
</table>

**Geometry**:

Chicago community boundaries

**Citation**: 

1. Anselin, Luc. 1995. “Local Indicators of Spatial Association — LISA.” *Geographical Analysis* 27: 93–115. 

2. Bivand, Roger. 2018. "r-spatial/spdep/localmoran." Github repository link: https://github.com/r-spatial/spdep/blob/master/R/localmoran.R.

3. Lansley,Guy and James Cheshire. 2016. "An Introduction to Spatial Data Analysis and Visualisation in R." *Consumer Research Data Centre*. 

4. GeoDa Center (https://geodacenter.github.io/data-and-lab//airbnb_Chicago-2015/), based on data from Chicago Data Portal. 

5. Inside Airbnb (http://insideairbnb.com/get-the-data.html).


## Future Work

Build up permutation and signficance filter function in R to clone permutation settings in GeoDa. Potential reference is the geary python script in <a href="https://github.com/pysal/pysal/blob/master/pysal/explore/esda/geary.py">pysal repository</a>.
