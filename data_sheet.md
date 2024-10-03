# Datasheet

Location:<br>
Human readable descriptive text:<br>
http://kaggle.com/datasets/puneet6060/intel-image-classification/data
<br>A compressed ZIP archive can be downloded from here:<br>
http://kaggle.com/datasets/puneet6060/intel-image-classification/download
<br>In the Jupyter Notebook, **_intel-image-classification.zip_** is automatically and temporarily downloaded (346 MB), if the dataset does not already exist locally. This ZIP file is deleted after all the images are extracted.

## Motivation

- **For what purpose was the dataset created?** 
    - The dataset was created to provide a benchmark for image classification algorithms, specifically for classifying natural scenes. It was also used for a competition hosted on Analytics Vidhya.
- **Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)? Who funded the creation of the dataset?**
    - The dataset was created by Intel and initially published on [Analytics Vidhya](http://analyticsvidhya.com) for an image classification challenge.

## Composition

- **What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)?**
    - The dataset consists of images representing six classes of natural scenes: buildings, forest, glacier, mountain, sea, and street.
- **How many instances of each type are there?**
    - The dataset contains approximately 25,000 images in total. The exact number of images per class is not specified but is roughly balanced across the six categories. 
- **Is there any missing data?**
    - There is no mention of any missing data in the dataset description.
- **Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by    doctor–patient confidentiality, data that includes the content of individuals’ non-public communications)?**
    - No, the dataset consists of images of natural scenes and does not contain any confidential information.

## Collection process

- **How was the data acquired?**
    - The images were likely collected from various sources, although the specific details of the acquisition process are not explicitly stated.
- **If the data is a sample of a larger subset, what was the sampling strategy?**
    - It is unclear if the dataset is a sample of a larger subset. If it is, the sampling strategy is not provided.
- **Over what time frame was the data collected?**
    - The time frame over which the data was collected is not specified.

## Preprocessing/cleaning/labelling

- **Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)? If so, please provide a description. If not, you may skip the remaining questions in this section.**
    - The images were resized to approximately 150x150 pixels but htey appear in various sizes - smallest 76x150 to biggest 150x150 pixels.
    - The images were labelled into the six categories.
- **Was the “raw” data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)?**
    - It is not mentioned if the raw data was saved.

## Uses

- **What other tasks could the dataset be used for?**
    - The dataset could be used for various computer vision tasks like:
        - Transfer learning for other image classification tasks.
        - Developing and evaluating new image classification algorithms.
        - Image segmentation and object detection.
        - Scene understanding and analysis.
- **Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses? For example, is there anything that a dataset consumer might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g., stereotyping, quality of service issues) or other risks or harms (e.g., legal risks, financial harms)? If so, please provide a description. Is there anything a dataset consumer could do to mitigate these risks or harms?**
    - As the dataset consists of natural scenes, there are no immediate ethical concerns regarding bias or unfair treatment. However, users should be aware of potential biases in the dataset, such as under-representation of certain geographical locations or environments, which could affect the performance of models trained on this data when applied to different contexts.
- **Are there tasks for which the dataset should not be used? If so, please provide a description.**
    - The dataset should not be used for tasks that require identifying specific individuals or sensitive information, as it does not contain such data.

## Distribution

- **How has the dataset already been distributed?**
    - The dataset was initially distributed through Analytics Vidhya for a competition and is now available on Kaggle.
- **Is it subject to any copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?**
    - The dataset is likely subject to some terms of use, but the specific details are not mentioned. Users should refer to the Kaggle platform and any associated license agreements for more information.

## Maintenance

- **Who maintains the dataset?**
    - The dataset is currently maintained on Kaggle, but it is unclear whether Intel or Analytics Vidhya continue to play an active role in its maintenance.
