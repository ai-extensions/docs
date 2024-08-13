# User Scenario 10 - Eric discovers a model and consumes it

In this scenario, a stakeholder/user such as Eric is interested in discovering existing ML models, created by other researchers or practitioners such as Alice, for deploying and using it on an Exploitation Platform. Eric discovers a ML model by utilising the STAC search functionalities and narrowing down his search by providing key metadata, such as date and geographic location, as well as ML model-specific properties like model architecture or hyperparameters.

Once Eric identifies the service with the ML model that aligns with his project requirements, he interacts with the Platform Operator for deploying it as a processing service on an Exploitation Platform. After successful deployment, Eric can find the service among those available on the Exploitation Platform, and can execute it with his own datasets, allowing integration in his own geospatial analysis workflows.

The requirements defined in the User Scenario 10 are:

* Import Libraries (e.g. `pystac`, `boto3`).
* Search ML model with `pystac` by defining specific metadata parameters.
* Configure Exploitation Platform (e.g. GEP) and deploy inference service as a processing service (supported by the Platform Operator).
* Launch a new job and monitor its execution.
* Check job status and retrieve results.

The link to the Notebook for User Scenario 10 is: [https://github.com/ai-extensions/notebooks/blob/main/scenario-10/s10-search_executeMLmodel.ipynb](https://github.com/ai-extensions/notebooks/blob/main/scenario-10/s10-search_executeMLmodel.ipynb).

For more information and practical examples, see the related article [**Discovering, deploying and consuming an ML model**](https://discuss.terradue.com/t/announcing-the-launch-of-the-ai-ml-enhancement-project-for-gep-and-urban-tep-exploitation-platforms/1188/14#aiml-enhancement-project-discovering-deploying-and-consuming-an-ml-model-1). 