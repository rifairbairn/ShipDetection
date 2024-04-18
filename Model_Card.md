# Model Card for Airbus Ship Detection
## Model Description
**Input:** The model accepts color images (RGB) with dimensions 768x768 pixels. Each input image is a photograph taken from satellite.

**Output:** The model outputs a binary classification result:
1: Indicates the presence of a ship within the image.
0: Indicates the absence of any ship within the image.

**Model Architecture:** The model uses the ResNet50 architecture, which is a convolutional neural network that is 50 layers deep. The model was pre-trained on the ImageNet dataset and adapted for binary classification with a custom fully connected layer to output the binary decision.

## Performance
The model achieves an accuracy of 91% on the test set, which consists of randomly selected images from the original dataset that were not used during training. The performance metric used is binary classification accuracy, which measures the percentage of correctly predicted images out of the total number of images in the test set.
![image](https://github.com/rifairbairn/ShipDetection/assets/77961773/736c4054-4a05-4b26-b876-2062baa6fa1c)

## Limitations
Limitation: The model's performance heavily depends on the quality and variety of the data. In scenarios where ships are partially obscured, there are large waves or there is significant glare, the model's accuracy might decrease. The might also not perform well if the images taken from different angles or different level of zoom.

## Trade-offs
Accuracy vs. Speed: While ResNet50 provides a robust framework for accurate image classification, it is computationally intensive and not takes a significant amount of time to train on such a large dataset.
Generalization vs. Specialization: The model is specialized for detecting ships in specific types of satellite images and may not generalize well to other types of image format or object detection without retraining or fine-tuning.
