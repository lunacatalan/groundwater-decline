# Climatic Trends and Agriculture Expansion on Declining Water Levels in Arid Aquifer, Iran
This analysis can help guide groundwater management strategy by shedding light on how different factors are contributing to the rapid decline, with the hope of developing effective management strategies to protect groundwater resources.

## Goals
- Identify the role of precipitation trends and changes in agriculture production on groundwater level declines in Qazvin Aquifer, Iran
- Run regression models using `lm()` on these factors of interest to determine statistical significance
- Practice hypothesis testing

## Visualizations

There are two main visualizations in this repository. The first shows a time series graph of area equipped for irrigation, and groundwater level changes from the years 1984-2019. The second is a plot of the median soil adjusted vegetation index (SAVI) value across the buffered area over time. 

## Skills Highlights
- Statistical analysis in R using `lm()` to run simple and linear regressions
- Hypothesis testing 
- Using ArcGIS to build shapefiles with reference aquifer maps
- Raster data manipulation
- Geospatial analysis of Landsat data in Python
- Calculating geospatial summary statistics using satellite data in Python

# Limitations and Future Analysis 
**IMPORTANT LIMITATIONS**

I was only able to calculate the relationship between median SAVI and groundwater level change. The positive relationship between these variables is surprising, since I expected that an increase in SAVI would lead to greater negative groundwater change. My analysis does not take into account a possible **lag** in the effect of groundwater-fed irrigation on crop production (which influences SAVI values) and groundwater level changes. This relationship may also be explained by a possible quadratic fit for the median SAVI values over time. Around the early 2000's, the median SAVI values begin to show an upward trend. This is supported by the literature that indicates that agriculture activities have become more expansive. Given more time I would have liked to explore this potential trend.

Furthermore, I used available literature to decide on the month that I would select to investigate the soil adjusted vegetation index. I selected the month when a majority of the crops were going to be harvested, as I assumed that it would be the best measure of amount of agricultural production. A more specific measure would involve analyzing landsat images over the whole year, over time, to see what the reflectance values for that specific area were, and how those values correlated with crop production on the ground. I was unable to conduct that land classification.

**ANALYSIS OF GROUNDWATER DECLINES**

In a future analysis I would like to collect depth to groundwater data for multiple wells over time, and see if there is a spatial relationship with changes in agriculture over that same time period (eg. shifting crop types, expansion or decline of area cultivated, irrigation system). Ideally, I could group these aquifers into climate types (eg. arid) so that any relationships could be understood within the type of climate that the aquifer is in. This would provide insight into the mechanisms of groundwater decline and a roadmap to uncover groundwater management strategies in areas where there is either no groundater decline or levels are in recovery.

It would also be interesting to obtain more data on groundwater level from wells around different aquifers and use Kriging to identify the spatial correlation between groundwater levels and different land cover types around the aquifer. Identifying how different land-cover types impact groundwater can be important considerations for future development.


## Contents/Structure:


    groundwater-decline
        │ README.md 
        | agriculture_landsat.ipynb
        │ Rmd/Proj files
        │ 
        └───data 
             │ AEI_ASC
                  | .ASC files
             │ ag_density
                  | buffer_df.csv
                  | aq_df.csv
             │ annual_precip.xlsx
             │ qazvin
                  | aquifer shapefile folder
             │ qazvin_aquifer_image


Data Download Instructions:

**IMPORTANT** 

Some of the data associated with this assignment is too large to
include in the GitHub repo. Data should be stored locally and added to
.gitignore file. Download the Area equipped for irrigation data in the `AEI_ASC` folder from
[here](https://zenodo.org/records/7809342).

The annual precipitation data can be accessed from this citation: Karger, D.N., Wilson, A.M., Mahony, C., Zimmermann, N.E., Jetz, W. Global daily 1km land surface precipitation based on cloud cover-informed downscaling. Scientific Data doi.org/10.1038/s41597-021-01084-6 (2021).



