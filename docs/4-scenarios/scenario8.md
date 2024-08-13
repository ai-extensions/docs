# User Scenario 8 -​ Alice reuses an existing pre-trained model

This notebook demonstrates the process of reusing a pre-trained model by leveraging the power of transfer learning. Transfer learning, a widely adopted technique in deep learning, involves using an existing model, pre-trained on a large dataset (such as ImageNet), to train a new model on a smaller, task-specific dataset. This approach allows the new model to effectively utilize the features learned by the pre-trained model, enabling it to extract valuable information from the input data more efficiently. Consequently, the new model can achieve higher accuracy even with limited data.

This implementation was performed for a semantic segmentation task in the scope of Earth Observation (EO). The process involves searching and downloading a suitable EO dataset already annotated by experts and that includes both EO data (in this case Sentinel-2 data) and their corresponding masks. After performing the appropriate feature engineering on the data, the user fine-tuned the pre-trained model to provide high-resolution results. This step could leverage the GPU resources set-up in the dedicaetd App Hub environment (with the **Machine Learning Lab with GPU 0.10** profile), significantly reducing the execution time for fine-tuning. Finally, the model was assessed and tested on unseen data.

The requirements defined in the User Scenario 8 are:

* Import libraries (e.g. torch, sklearn, albumentation).
* Data acquisition, including EO data search and data loader implementing different augmentation techniques (e.g., RandomCrop, Resize, and RandomRotate90) and data loading in batches.
* Data visualization to enable the user to gain comprehensive insights of data distribution.
* Selection of pre-trained ML model, in this case with a UNet backbone trained on ImageNet, and subsequently implementation of fine-tuning adjustments.
* Evaluation of outputs using different techniques on unseen dataset (e.g., plotting loss functions, calculating mIOU).
* Inference on the unseen test dataset.