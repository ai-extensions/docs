# User Scenario 3 - Alice describes the labelled Earth Observation data

Labeled Earth Observation (EO) data can be described using the SpatioTemporal Asset Catalog (STAC) standard. This allows to describe the labeled EO data while defining standardized sets of metadata to delineate its key properties, such as spatial and temporal extents, resolution, and other pertinent characteristics. Additionally, it enables the user to include details about the labeling process itself, as well as enabling specific parameters-driven queries on the catalog.

The requirements defined in the User Scenario 3 are:

* Import libraries, including those for connecting to STAC API (e.g. `pystac`).
* Load labelled data (e.g. `.geojson` files).
* Create a STAC Item for each labelled EO data, including relevant metadata and STAC Extensions to describe the labelled data (e.g. the `stac-extensions/label extension` to provide detailed labelling information, or the `stac-extensions/asset` to associate assets or additional files with the labelled data).
* Extract metadata of the created STAC item, and show its relevant information, including visualisation on spatial map.

The link to the Notebook for User Scenario 3 is: ​​https://github.com/ai-extensions/notebooks/blob/main/scenario-3/s3-describingEOdata.ipynb.