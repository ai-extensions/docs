# User Scenario 5 - Alice develops a new Machine Learning model

During the implementation of this Scenario, two Notebooks were developed:

* **“Alice develops a new machine learning”** Notebook: this is the main Notebook for Scenario 5, as it follows the requirements for Scenario 5 described in the Service Specification document. 
* **“Implementation of EuroSAT STAC dataset”** Notebook: the objective of this Notebook was to generate STAC Catalog, Collection and Items of the EuroSAT dataset. The EuroSAT STAC dataset was then used as input dataset for developing and testing the main **“Alice develops a new machine learning”** Notebook. 

## Notebook for **“Alice develops a new machine learning”**
The AI-user employs MLflow Tracking as a crucial tool throughout the ML model development cycle. It ensures effective log tracking and preserves vital information, including specific code versions, datasets used, and model hyperparameters. By logging this information, the reproducibility of the work drastically increases, enabling users to revisit and replicate past experiments accurately. Moreover, quality metrics have been tracked during the task, such as classification accuracy, loss function fluctuations, and inference time, enabling easy comparison between different models.

A pivotal component of the platform is the Model Registry, which is seamlessly integrated with the experiment tracking functionality. The Model Registry acts as a central repository, allowing the user to manage and oversee their models effectively. This preservation of trained models is of significant economic importance, as training a model often requires substantial time and computing resources.

The requirements defined in the User Scenario 5 that were included in this Notebook are:

* Import Libraries (e.g. `tensorflow`, `mlflow`, `sklearn`)
* Clarify the specific problem, identify the input data, and provide a pipeline for data ingestion. This ensures training a high-resolution classifier.
* Design the model architecture with the advantage of Convolutional Neural Networks (CNNs). The architecture may encompass different hidden layers with a variety of activation functions (such as *ReLU, Sigmoid, tanh*) and a couple of techniques that enhance the stability and reliability of the model, such as Batch Normalization and Regularization (namely Dropout).
* Train the model using the EuroSAT STAC training dataset and evaluate the performance of the trained model on the test dataset. 
* Evaluate the ML model with evaluation metrics such as accuracy, precision, recall, F1 score, and the confusion matrix, in order to determine the model's effectiveness.
* Fine-tune the ML model by adjusting hyperparameters, modifying the architecture, or incorporating regularization techniques, as needed. This step may be repeated several times to reach the best performance and log the impact of each adjustment on the performance of the output model. 
* Use MLflow Tracking tools (e.g. autolog functionality) to log relevant information such as hyperparameters, model configurations, training metrics, model weights, and evaluation results using MLflow APIs. 

The link to this Notebook is: ​[​https://github.com/ai-extensions/notebooks/blob/main/scenario-5/trials/s5-newMLModel.ipynb](​https://github.com/ai-extensions/notebooks/blob/main/scenario-5/trials/s5-newMLModel.ipynb).

For more information and practical examples, see the related article [**Developing a new ML model and tracking with MLflow**](https://discuss.terradue.com/t/announcing-the-launch-of-the-ai-ml-enhancement-project-for-gep-and-urban-tep-exploitation-platforms/1188/8). 

## Notebook for **“Implementation of EuroSAT dataset STAC”**
The EuroSAT dataset is based on ESA's Sentinel-2 data, covering 13 spectral bands and consisting out of 10 classes with a total of 27,000 labeled and geo-referenced images ([https://github.com/phelber/EuroSAT](https://github.com/phelber/EuroSAT)). This Notebook was used to create a STAC Catalog, a STAC Collection, and STAC Items for the entire EuroSAT dataset. Each STAC Item was generated with three assets: the EuroSAT's georeferenced patches (in .tif format), their labels (in `.geojson` format), and their RGB-composite thumbnails (in `.jpeg` format). These STAC objects were posted into ESA-AI dedicated S3 bucket (s3://ai-ext-bucket-dev/), and subsequently posted on the ESA-AI dedicated STAC endpoint ([https://ai-extensions-stac.terradue.com](https://ai-extensions-stac.terradue.com)). 

The requirements that were included in this Notebook are:

* Import Libraries (e.g., `pystac`, `torchgeo`).
* Load the EuroSAT/EuroSAT100 Dataset using the torchgeo API. 
* Generate STAC objects (STAC catalog, STAC collection, and STAC Item) with their corresponding characteristics, namely, id, properties, assets, STAC extensions, etc., using pystac standard conventions and place them in a .json file. The class label for each patch of data is stored in a `.geojson` file format.
* Post the generated STAC objects into the S3 bucket s3://ai-ext-bucket-dev.
* Publish all STAC items into the dedicated collection “EUROSAT_2024_dataset” in the STAC endpoint ([https://ai-extensions-stac.terradue.com](https://ai-extensions-stac.terradue.com)), and then validate by checking the published items.

The link to the Notebook for User Scenario 5 is: [https://github.com/ai-extensions/notebooks/blob/main/scenario-5-stac-dataloader/s5-stac-dataloder.ipynb](https://github.com/ai-extensions/notebooks/blob/main/scenario-5-stac-dataloader/s5-stac-dataloder.ipynb). 