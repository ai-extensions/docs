# User Scenario 6 - Alice starts a training job on a remote machine

In this scenario, the ML practitioner Alice develops two Earth Observation (EO) Application Packages using the Common Workflow Language (CWL), as described in the OGC proposed best practices. The two App Packages CWLs are executed on a remote machine with a CWL runner for Kubernetes, enabling the submission of (parallel) kubernetes jobs distributed across the available resources in the cluster. MLflow is used for tracking experiments and related metrics for further analysis and comparison.

* **App Package CWL for a training job**: Alice develops an ML training job with `RandomForest`, based on a segmentation approach for water bodies masking. The training process is repeated and evaluated for each training run with MLflow and in the end, the model evaluated with higher performance is selected and used for the inference service.
* **App Package CWL for inference job**: this service performs inference on Sentinel-2 data, based on the best model developed with the training service. It takes as input parameter the STAC Item(s) of Sentinel-2 data and generates the inference water-bodies output mask(s).

The requirements defined in the User Scenario 6 are:

* Write a Python application with its containerised environment
* Use the CWL standard, as described in the OGC proposed best practices, for writing EO Application Packages
* Dockerise all processing nodes and write the App Package CWLs through CI/CD pipeline with GitHub Actions, and release them as official repository releases
* Use the CWL runners for Kubernetes to submit (parallel) jobs, distributing them across the available resources in the cluster
* Configure MLflow server for tracking the experiments and log relevant information

The links to the App Package CWL files are: 

* **App Package CWL for training job**: https://github.com/ai-extensions/notebooks/releases/download/v1.0.8/water-bodies-app-training.1.0.8.cwl 
* **App Package CWL for inference job**: https://github.com/ai-extensions/notebooks/releases/download/v1.0.8/water-bodies-app-inference.1.0.8.cwl 

For more information and practical examples, see the related article [**Training and Inference on a remote machine**](https://discuss.terradue.com/t/announcing-the-launch-of-the-ai-ml-enhancement-project-for-gep-and-urban-tep-exploitation-platforms/1188/9#aiml-enhancement-project-training-and-inference-on-a-remote-machine-1). 