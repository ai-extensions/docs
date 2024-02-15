# User Scenario 2 - Alice labels Earth Observation data

Labelling data is a crucial step in the process for developing supervised Machine Learning (ML) models. It involves the critical task of assigning relevant labels or categories to different features within the data, such as land cover class (e.g. vegetation, water bodies, urban area, etc.) or other physical characteristics of the Earth's surface. These labels can be binary (e.g., water or non-water) or multi-class (e.g., forest, grassland, urban).

The requirements defined in the User Scenario 2 are:

* Import libraries for data manipulation (e.g. `pandas`), visualisation (e.g. `matplotlib`,`seaborn`), geospatial analysis (e.g `rasterio`).
* Create labelling layers, using e.g. QGIS or an interactive map based on `Leafmap`, by creating new vector layers or annotations to mark the labelled areas or features, and export them in formats suitable for further analysis or machine learning tasks, such as shapefiles, GeoJSON, or raster formats.
* Connect to STAC API for accessing to Sentinel-2 data, using appropriate authentication credentials.
* Query and retrieving the Data using specific parameters to filter out retrieved data (e.g time range, spatial extent, cloud cover).
* Validate the labelled data to ensure its accuracy and reliability, comparing it to a reference dataset.
* Use Labelled Data for Supervised Machine Learning to train models, evaluate their performance, and make predictions on new, unlabeled EO data.

The link to the Notebook for User Scenario 2 is: ​[​https://github.com/ai-extensions/notebooks/blob/main/scenario-2/s2-labellingEOdata.ipynb](​https://github.com/ai-extensions/notebooks/blob/main/scenario-2/s2-labellingEOdata.ipynb).