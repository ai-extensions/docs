# User Scenario 4 - Alice discovers labelled Earth Observation data

This Scenario documents the process for discovering labelled EO data described with the STAC standard. One of the notable advantages of the STAC-supported catalogs is the ability to filter search results using STAC metadata. This empowers the user to narrow down the search based on specific labeling criteria. By applying such filters, the user can pinpoint the datasets that align with the specific requirements.

This Scenario explores two ways to discover, query and access labeled EO datasets: by using the STAC Browser, which provides a user-friendly graphical interface, or by using the STAC API endpoint, which enables the user to access to the STAC collection programmatically. 

The requirements defined in the User Scenario 4 are:

* Import Libraries (e.g. `pystac`).
* Understand about the STAC standard.
* Interact with a STAC Browser tool or the STAC API endpoint to access STAC data, by defining the search criteria based on the requirements (e.g. time range, geographic extent, etc.).
* Examine the search results to explore the available labeled EO datasets (view metadata summaries) and identify a dataset that meets the requirements to access associated assets.
* Depending on the access permissions and licensing, the user identifies labelled EO a dataset stored on AWS S3 bucket and is given the option to either download it or integrate it into the workflow for further analysis or model training.

The link to the Notebook for User Scenario 4 is: ​​https://github.com/ai-extensions/notebooks/blob/main/scenario-4/s4-discoveringLabelledEOData.ipynb.