# Biodiversity_Intactness_Phoneix_AZ
A brief analysis and visualization of the changes in biodiversity intactness from 2017 to 2020 in Phoneix, Arizona.

## Data Analysis Objectives:

- Utilize the Planetary Computer STAC catalog to access the `io-biodiversity` data for 2017 and 2020, and load it in using `pystac_client`.

- Create a map of Phoenix County from US National Census data boundaries, and use `contextily` to provide greater context for the boundary with an appropriate basemap.

- Find areas with BII loss of at least 75% from 2017 to 2020, and use the `matplotlib.color` package to assign a cmap for the data represnted as 0 (not 75%) or 1 (at least 75%) values.

- Visualizing the difference in BII loss between 2017 and 2020, and use the `matplotlib.lines` package to create a legend, indicating which pixels were present in the 2017 data but not in the 2020.

## Repository Structure:

- This repository contains only the notebook which runs through how to complete the 'Data Analysis Objectives' above. To preserve the function of this github repository, the data has not been uploaded, but the contents are available through the links provided in the references section down below. Therefore, the .gitignore file omits the data folder. 

```
Biodiversity_Intactness_Phoenix_AZ
│   README.md
|   biodiversity_impact.ipynb
|   .gitignore
```

## Data:
#### Biodiversity Index:
- This dataset was last accessed on December 7th, 2024 from the Microsoft Planetary Computer (MAPC) website, but was originally complied from ImpactObsaervation and Vizzuality. 
Please note that this file will contain the biodiversity intactness data from around the world, and must be clipped to area of interest.

- The Biodiversity Intactness Index from Planetary Computer is an estimation of species abundance, richness, counts, and 'Compositional Similarity', which compares each sample ecosystem to an intact baseline. The methods utilized to estimate spatial biodiversity were developed in the paper “Global 100m Projections of Biodiversity Intactness for the years 2017-2020.”

- This data used for modeling was sampled across 32,000 sites over 750 individual studies, and compiled into the PREDICTS database. Using this STAC collection, we can compare the Biodiversity Intactness Index for different locations or, in our case, the same location across different years.

#### Phoenix, AZ TIGER/Line Shapefile:
- This dataset was last accessed on December 7th, 2024 from the Data.gov website. The other organizations listed as the main producers of the data are the US Department of Commerce, the Geospatial products branch of the US Census Bureau, and the Geography Division of the US Census Bureau. 

- To visualize our region of interest, we downloaded a shapefile of the counties in Arizona and filter to geometries from the Phoenix area. This data is compiled by the U.S. Census Bureau's Master Address File / Topologically Integrated Geographic Encoding and Referencing (MAF/TIGER) Database (MTDB).

- Please note that the geometries in this file cover the entirety of the state of Arizona, and must be filtered to the desired county. 


## Resources:

#### MAPC STAC Catalog io-biodiversity Dataset
Microsoft Planetary Computer, STAC Catalog. Biodiversity Intactness. (2024). [Dataset]. https://planetarycomputer.microsoft.com/dataset/io-biodiversity. date accessed [12/07/2024]

#### TIGER/Line Shapefile of the Arizona Boundary, from US Census Collection
United States Census Bureau. (2023. Arizona County TIGER/Line Shapefiles. [Dataset]. United States Census Bureau. https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html. date accessed [12/07/2024]

#### MEDS Program at UCSB: EDS 220 Working With Environmental Datasets:
Galaz Garcia, C. (2024). Final Project, EDS 220 Working With Environmental Datasets, Masters of Environmental Data Science. University of California, Santa Barbara. 
https://meds-eds-220.github.io/MEDS-eds-220-course/assignments/assignment4.html. date accessed: [12/07/2024] 
