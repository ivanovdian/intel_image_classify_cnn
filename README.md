# CNN Classification of Scene Images using the Intel Image Classification dataset

## BUSINESS GOALS
This project aims to classify natural scene images into six categories: buildings, forest, glacier, mountain, sea, and street. The Intel Image Classification dataset is utilised to develop a deep learning model capable of automatically identifying the type of scenery in a given image. This technology has practical applications in various fields, such as travel photography organisation, environmental monitoring, and automated image tagging for content management systems.

## DATA
Location:<br>
Human readable descriptive text:<br>
http://kaggle.com/datasets/puneet6060/intel-image-classification/data
<br>A compressed ZIP archive can be downloaded from here:<br>
http://kaggle.com/datasets/puneet6060/intel-image-classification/download
<br>In the Jupyter Notebook, **_intel-image-classification.zip_** is automatically and temporarily downloaded (346 MB), if the dataset does not already exist locally. This ZIP file is deleted after all the images are extracted.

The dataset used is the Intel Image Classification dataset is available on Kaggle (link above). It contains approximately 25,000 images of intended size 150x150 pixels, distributed across six classes: buildings, forest, glacier, mountain, sea, and street.

In practice, it turns out, these colour images of scenes from all over the world are found to be with various dimensions - smallest 76x150 to biggest 150x150 pixels.

The dataset is split into training (14,000 images), testing (3,000 images), and prediction (7,000 images) sets. This diverse collection of natural scene images provides a robust foundation for training and evaluating the classification model.

## MODEL 
A Convolutional Neural Network (CNN) architecture is employed for this image classification task. The model consists of three convolutional layers followed by max pooling and three dense (fully connected) layers. This architecture is chosen for its proven effectiveness in image recognition tasks and its ability to learn hierarchical features from the input images. The model uses ReLU activation functions in the hidden layers.

## HYPERPARAMETER OPTIMISATION
Several hyperparameters are optimised to enhance model performance:

- **Learning rate**: Utilises a learning rate scheduler that reduces the rate on plateau.
- **Dropout Rate**
- **Weight Decay** aka 'l2_lambda'

These hyperparameters are derived after using an automatic Optuna tuning procedure where empirical testing and common practices in deep learning for image classification tasks are employed.

Fixed hyperparameters:

- **Batch size**
- **Epochs**: Trained for 45 epochs with early stopping to prevent overfitting.
- **Optimiser**: Adam optimiser is used for its adaptive learning rate capabilities.

## RESULTS
The model achieves a very good accuracy of 84%  on the test validation data sub-set. The confusion matrix and classification report reveal strong performance across all classes, with some minor confusion between visually similar categories (e.g., sea and glacier). The model demonstrates high precision and recall for most classes, indicating its reliability in real-world applications.

The Confusion Matrix is available for closer examination in the **_model_card.md_** file of this project.

Key insights from the results:
- The model excels at identifying forest and street scenes.
- There is room for improvement in distinguishing between mountain and glacier scenes.
- The balanced performance across classes suggests that the model has learned generalisable features for each category.

These results indicate that the CNN model is highly effective for classifying natural scene images and could be valuable in various applications requiring automated image categorisation.

## CONTACT DETAILS
For more information or inquiries about this project, please contact:<br>
[Linkedin](http://linkedin.com/in/dian-ivanov-5321561)
