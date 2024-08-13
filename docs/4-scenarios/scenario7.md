# User Scenario 7 ​- Alice describes her trained machine learning model

This Scenario leverabes the capabilities of STAC to provide a comprehensive and standardised description of a trained ML model. This is done with a STAC Item file that encapsulates the relevant metadata, such as: model name and version, description of the model architecture and training process, specifications of input and output data formats, performance metrics and evaluation results, details regarding model deployment and usage. This approach not only facilitates collaboration but also promotes interoperability within the geospatial and ML communities.
extensions

The requirements defined in the User Scenario 7 are:

* Import Libraries (e.g. `pystac`, `boto3`).
* Option to either create a STAC Item with `pystac`, or to upload an existing STAC Item into the Notebook. The STAC Item will contain all related ML model specific properties, related STAC extensions and hyperparameters.
* Create interlinked STAC Item, Catalog and Collection, and the STAC folder structure.
* Post STAC files onto S3 bucket.
* Publish STAC files onto STAC endpoint.
* Search STAC items on STAC endpoint with standard query params such as bbox and time range, but also with ML-specific params such as model architecture, hyperparameters.