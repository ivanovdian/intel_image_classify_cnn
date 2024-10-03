# Model Card

## Model Description

**Input:** The model takes colour images of scenes from all over the world with various dimensions - smallest 76x150 to biggest 150x150 pixels. These images are not resized to match the input requirement of the CNN architecture as the CNN deals with this internally by dynamically catering for each image it processes. The task for this model is to classify the non-classified images in the "pred" sub-dataset. 

**Output:** The model outputs a probability distribution over six classes: 'glacier', 'street', 'mountain', 'forest', 'sea', 'buildings'. The randomly picked images from the "pred" sub-dataset is predicted to be a member of one of the six classes and is plotted at the end.

**Model Architecture:** The model is a modified dynamic and enhanced LeNet-5, with the following changes:
- Input colour images are not resized to match the input requirement of the CNN. The images are with various demotions - smallest, 76x150 to biggest 150x150 pixels.
- A third convolutional layer is added for better training performance.
- The first fully connected layer dynamically adjusted if necessary to accommodate the various shapes and sizes of the images.
- The final fully connected layer is modified to output predictions for the six classes noted above.
- The Adam optimiser is used instead of SGD for better convergence and performance.
- Various hyperparameter optimisation tweaks are implemented in the architecture for automated Optima hyperparameter tuning.

## Performance

The model performs very well. Being trained on fourteen thousand samples and validated against three thousand samples the observed confusion matrices and accuracies are nearly 99% and 84% respectively. The data consists of numerous and wide examples of real-life scenes and it would seem that the model generalises well from all the complex data available. The predicted random samples from the non-classified data samples seem to hit the mark 100%, although, admittedly, with the size of the prediction random sample set to 10, more predictions are needed so true performance can be observed:
![train_loader_confusion_matrix_and_accuracy](train_loader_confusion_matrix_and_accuracy.png)
![validationtest_loader_confusion_matrix_and_accuracy](validationtest_loader_confusion_matrix_and_accuracy.png)

## Limitations
Although Overfitting is always a risk, looking at the performance metrics above would suggest that this is minimal.<br>
The original training data is almost evenly biased as seen in the Jupyter Notebook bar chart plot of the data classes.<br>
The model, it would seem, is able to predict and generalise, and is well placed to handle any image presented, even a new picture, taken today, from a smartphone.

## Trade-offs

- The dataset is admittedly a bit large for this starting level CNN model, where only a single additional layer was introduced. The time taken to tune the hyperparameters and the train the model took a bit of time even on a GPU. There are better models out there that would take much less time.
- From the optimiser literature available, SGD (Stochastic Gradient Descent) with momentum offers better generalisation but slower convergence, ideal for large datasets. ADAM (Adaptive Moment Estimation) converges faster with adaptive learning rates but may overfit and generalise poorly in some cases. However, in this case, for this model in particular, using the ADAM optimiser worked well and overfitting and poor generalisation were not observed.
- Accuracy vs. Generalisation - it would appear this model is acceptable regarding this consideration.
