# ShipDetection

## NON-TECHNICAL EXPLANATION
This project aims to automatically identify images that contain ships using advanced machine learning techniques. By analyzing satellite photos, we can determine the presence of ships, which has applications in maritime safety, traffic monitoring, and environmental studies. We use a technique known as deep learning, which allows the computer to recognize patterns and features in images that are indicative of ships.

## DATA
The model is trained on the Airbus Ship Detection Dataset, which contains satellite images of ships. This dataset is publicly available and is often used for object detection challenges in the machine learning community. Each image is labeled to indicate whether or not it contains a ship, allowing the model to learn from these examples.

Source: Airbus Ship Detection Challenge on Kaggle (https://www.kaggle.com/competitions/airbus-ship-detection)

## MODEL
We utilize the ResNet50 model, a powerful deep neural network known for its effectiveness in image classification tasks. ResNet50 is chosen for its deep architecture and ability to learn rich feature representations for complex visual tasks. The model has been pre-trained on a large dataset (ImageNet) and fine-tuned on our specific ship detection dataset to tailor its capabilities to our needs.

## HYPERPARAMETER OPTIMISATION
We optimized several hyperparameters, including the learning rate, batch size, and number of training epochs. The optimization was performed using a grid search approach, where we systematically tested combinations of parameters to find the best performing configuration. This method ensures that the model not only learns effectively but also generalizes well to new, unseen images.

## RESULTS
The model achieved a high accuracy in detecting ships in satellite images, demonstrating its effectiveness for this task. The results indicate that the model can reliably distinguish between images with and without ships, which is crucial for practical applications. Here are some visualizations of the model predictions:

**Results here**

These insights help in refining the model further and in understanding the types of images where the model might need improvements.


