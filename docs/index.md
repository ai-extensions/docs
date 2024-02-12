# AI-Extension Application Hub - User Manual 

## Purpose

The AI-Extensions project aims at supporting the Earth Science and Services Communities by expanding the existing Earth Observation (EO) platform offerings services with operationally mature AI/ML software capabilities. This is achieved through the AI-Extension Application Hub, a dedicated Cloud platform that provides the integration and operational implementation of EO and AI capabilities.  

This User Manual provides a guideline, as well as step-by-step instructions, for developers and consumers to effectively leverage the AI-Extension Application Hub. 

## Registration

* App Hub URL: [https://app-hub-ai-extensions-dev.terradue.com/](https://app-hub-ai-extensions-dev.terradue.com/)
* User Registration: *add steps*
* JupyterHub - Server Options: different options can be configured for your username. These will be visible on the JupyterHub dashboard after login. In the example shown below, two server options are available. You can click on one (e.g. "**Machine Learning Lab 0.10 Large (12GB RAM)**") and click on `Start` to launch it. 

<p align="left" ><img src="../images/login_choice.png" alt="Picture" width="80%" height="100%"style=" display: block; margin: 20 auto;"/></p>
## Applications
### JupyterLab
After loading up, the JupyterLab dashboard will appear.

<p align="left" ><img src="../images/jupyterlab_dashboard.png" alt="Picture" width="80%" height="100%"style=" display: block; margin: 20 auto;"/></p>

### Code Server
Code Server enables the user to run Visual Studio Code (VS Code) and all its functionalities directly from the Application Hub. 

On the JupyterLab dashboard, click on the Code Server Logo.

<p align="left" ><img src="../images/codeserver_icon.png" alt="Picture" width="100" height="100"style=" display: block; margin: 20 auto;"/></p>

The Code Server dashboard will appear.

<p align="left" ><img src="../images/codeserver_dashboard.png" alt="Picture" width="80%" height="100%"style=" display: block; margin: 20 auto;"/></p>

You have access of all these functionalities from the vertical panel in the top-left corner of the dashboard:
* **Menu**: access functions and settings within VS Code
* **Explore**: navigate and manage files and directories in your workspace 
* **Search**: find specific files, text, or symbols within your workspace
* **Source Control**: manage version control system such as Git directly within VS Code
* **Run and Debug**: execute and debug code with built-in tools
* **Extensions**: enhance functionality by installing and managing extensions to support the development workflow 
* **Test**: run tests and view test outptus 

### ML-Flow
`MLflow` is a powerful open-source platform that simplifies the end-to-end machine learning (ML) lifecycle management. It provides tools for tracking experiments, model hyperparameters, packaging code into reproducible runs, and sharing and deploying models across different environments seamlessly. `MLflow` enables users to effectively organize and monitor their ML projects, enabling collaboration, reproducibility, and streamlined deployment workflows.

On the JupyterLab dashboard, click on the `mlflow` Logo.

<p align="left" ><img src="../images/mlflow_icon.png" alt="Picture" width="100" height="100"style=" display: block; margin: 20 auto;"/></p>

The `MLflow` dashboard will appear.

<p align="left" ><img src="../images/mlflow_dashboard.png" alt="Picture" width="80%" height="60%"style=" display: block; margin: 20 auto;"/></p>

Below are a few examples of using `MLflow` in a ML project workflow:
* The user can select one or multiple runs to **Compare**

<p align="left" ><img src="../images/selectrun.png" alt="Picture" width="60%" height="100%"style=" display: >block; margin: 20 auto;"/></p>

* The user can see a quick overview of each run and select which parameter(s) to analyse and plot on the graph

<p align="left" ><img src="../images/rundetails.png" alt="Picture" width="60%" height="100%" style=" display: >block; margin: 20 auto;"/></p>
       
* The user compares different parameteres fed to the CNN model

<p align="left" ><img src="../images/parameters.png" alt="Picture" width="60%" height="100%"style=" display: >block; margin: 20 auto;"/></p> 

* The user compares evaluation metrics of each run, to opt for the best model for his/her application. 

<p align="left" ><img src="../images/metrics.png" alt="Picture" width="60%" height="100%"style=" >display: >block; margin: 20 auto;"/></p>        

### QGIS

## Functionalities 
### Connection to STAC API
A dedicated STAC API endpoint was configured and can be access from the App Hub by providing the appropriate authorisation `headers`. 
```
cat = Client.open("https://ai-extensions-stac.terradue.com", headers=headers, ignore_conformance=True)
```
To show the available collections in the Catalog.
```
[c for c in cat.get_collections()]

[<CollectionClient id=ai-extensions-svv-dataset-labels>,
 <CollectionClient id=sentinel-s2-l2a-cogs>,
 <CollectionClient id=EUROSAT_2024_dataset>,
 <CollectionClient id=gisat-col>]
```

### Access to AWS s3
A dedicated Amazon S3 storage is pre-configured to be accessed from the App Hub. This can be done with the Amazon Web Server (AWS) `aws s3` commands in the AWS CLI.

For example, to list the content of a specific S3 bucket, you can use the command below.
```
aws s3 ls <bucket_name>
```
Other examples with full syntax on using the `aws s3` command are described in the official [AWS website](https://docs.aws.amazon.com/cli/latest/userguide/cli-services-s3-commands.html).