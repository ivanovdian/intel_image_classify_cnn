# Model Card

See the [example Google model cards](https://modelcards.withgoogle.com/model-reports) for inspiration. 

## Model Description

**Input:** The model takes coloyr images of sceens from al over the world with various dimations dimensions smallest, 76x150 to biggest 150x150 pixels. These images are not resized to match the input requirement of the CNN architecture as it deals with this internally by dynamically catering for each image it processes. The task is to classify the non-classified images in the "pred" sub-dataset. 

**Output:** The model outputs a probability distribution over six classes: 'glacier', 'street', 'mountain', 'forest', 'sea', 'buildings'. The randomply picked images from the "pred" sub-dataset is predicted to be a member of one of the six classes and is plotted at the end.

**Model Architecture:** The model is a modified version of LeNet-5, with the following changes:
- Input images are resized to 32x32 to match the LeNet-5 requirements.
- The final fully connected layer is modified to output predictions for two classes instead of the original 10.
- The original SGD optimizer is replaced with Adam for better convergence and performance.

## Performance

Give a summary graph or metrics of how the model performs. Remember to include how you are measuring the performance and what data you analysed it on. 

## Limitations

Outline the limitations of your model.

## Trade-offs

Outline any trade-offs of your model, such as any circumstances where the model exhibits performance issues. 
