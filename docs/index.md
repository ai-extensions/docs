# AI-Extension Application Hub - User Manual 

## Purpose

The AI-Extensions project aims at supporting the Earth Science and Services Communities by expanding the existing Earth Observation (EO) platform offerings services with operationally mature AI/ML software capabilities. This is achieved through the AI-Extension Application Hub, a dedicated Cloud platform that provides the integration and operational implementation of EO and AI capabilities.  

This User Manual provides a guideline, as well as step-by-step instructions, for developers and consumers to effectively leverage the AI-Extension Application Hub. 

## Registration

* App Hub url: [https://app-hub-ai-extensions-dev.terradue.com/](https://app-hub-ai-extensions-dev.terradue.com/)
* User Registration
* JupyterHub - Server Options: different options can be configured for your username. These will be visible on the JupyterHub dashboard after login. In the example shown below, two server options are available. You can click on one (e.g. "**Machine Learning Lab 0.10 Large (12GB RAM)**") and click on `Start` to launch it. 
<img src="../images/login_choice.png" width="800">

## Applications
### JupyterLab
After loading up, the JupyterLab dashboard will appear.
<img src="../images/jupyterlab_dashboard.png" width="800">

### Code Server
On the JupyterLab dashboard, click on the Code Server Logo.
<img src="../images/codeserver_icon.png" width="100">

The Code Server dashboard will appear.
<img src="../images/codeserver_dashboard.png" width="800">

### ML-Flow
On the JupyterLab dashboard, click on the ML-Flow Logo.
<img src="../images/mlflow_icon.png" width="100">

The ML-Flow dashboard will appear.
<img src="../images/mlflow_dashboard.png" width="800">

### QGIS

## Functionalities 
### Connection to STAC API

### Access to AWS s3
A dedicated Amazon S3 storage is pre-configured to be accessed from the App Hub. This can be done with the Amazon Web Server (AWS) `aws s3` commands in the AWS CLI.

For example, to list the content of a specific S3 bucket, you can use the command below.
```
aws s3 ls <bucket_name>
```
Other examples with full syntax on using the `aws s3` command are described in the official [AWS website](https://docs.aws.amazon.com/cli/latest/userguide/cli-services-s3-commands.html).
