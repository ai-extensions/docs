# User Scenario 1 - Alice does Exploratory Data Analysis (EDA)

The purpose of Exploratory Data Analysis (EDA) is to analyse the data that will be used to train and evaluate Machine Learning models. In this Notebook are firstly shown the steps to access and visualize EO data (e.g. Sentinel-2 scenes) and their metadata using STAC API. Secondly, a pre-arranged DataFrame containing labeled geospatial data with reflectance values and vegetation indices is loaded and used for the purpose of EDA.

The requirements defined in the User Scenario 1 are:

* Import Libraries for data manipulation (e.g. `pandas`), visualisation (e.g. `matplotlib`, `seaborn`), geospatial analysis (e.g `rasterio`).
* Connect to STAC API for accessing Sentinel-2 data and their metadata, as well as DataFrames that contain labelled geospatial data, using appropriate authentication credentials.
Query and retrieving the Data using specific parameters to filter out retrieved data (e.g time range, spatial extent, cloud cover).
* Visualising data (eg. S-2 metadata, spectral bands) and charts / graphs of the analysed relevant information (e.g. with `matplotlib`, `seaborn`). These are useful for gaining information about the data and for performing other tasks such as band combination, cloud masking, etc.
* Perform analysis on the EO data labels to gain insights and understand patterns. This includes tasks such as calculating statistical summaries, generating histograms or scatter plots, as well as making correlation matrix for understanding relationships between variables.
* Document and share of results and findings of the EDA process by exporting charts and visualisation plots into a report.

The link to the Notebook for User Scenario 1 is: [https://github.com/ai-extensions/notebooks/blob/main/scenario-1/s1-eda.ipynb](https://github.com/ai-extensions/notebooks/blob/main/scenario-1/s1-eda.ipynb)
