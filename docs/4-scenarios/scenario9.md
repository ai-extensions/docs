# User Scenario 9 - Alice creates a training dataset

This scenario demonstrates how to create a deep learning dataset using image chips. Annotating a dataset is a meticulous and time-consuming process that demands precision and focus. To ensure accuracy, the dataset must be reviewed by multiple experts. However, various computer vision techniques can expedite this process. For instance, an initial labeling can be done by another ML model, with human experts refining these labels to ensure their correctness.

In this Scenario, the user generates a labelled dataset for a semantic segmentation task using:

* a human-annotation approach with the IRIS Tool, an AI-assisted tool that enhances image segmentation and classification for satellite imagery and other types of images, developed by ESA/ESRIN Phi-Lab (see [documentation](https://github.com/ESA-PhiLab/iris)).
* an automated ML-driven approach consisting on a `RandomForest` model for segmenting task. 

The process of creating the training dataset is finalised with the creation of the STAC objects of each data (i.e. the generated image patches and their corresponding masks), and the related publication on a dedicated S3 bucket and STAC endpoint.

The requirements defined in the User Scenario 9 are:

* Import libraries (e.g., `pystac`, `rasterio`, `boto3`, `sklearn`).
* Load the Sentinel-2 data using STAC.
* Generate EO image patches with their corresponding masks (annotated with three classes `water`, `non-water` and `not-applicable`), using both an AI-driven approach and an human-annotation approach.
* Create STAC Objects, including STAC Item for each image patch, STAC collection, and STAC catalog to describe the dataset with its metadata.
* Post the STAC Objects to a dedicated S3 bucket.
* Publish the STAC Objects into a dedicated STAC endpoint.

The link to the Notebook for User Scenario 9 is: [https://github.com/ai-extensions/notebooks/blob/main/scenario-9/s9-CreatingTrainingData.ipynb](https://github.com/ai-extensions/notebooks/blob/main/scenario-9/s9-CreatingTrainingData.ipynb).

For more information and practical examples, see the related article [**Creating a training Dataset**](https://discuss.terradue.com/t/announcing-the-launch-of-the-ai-ml-enhancement-project-for-gep-and-urban-tep-exploitation-platforms/1188/13#aiml-enhancement-project-creating-a-training-dataset-1).