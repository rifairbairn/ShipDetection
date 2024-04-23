# ShipDetection

## Non-technical Explanation
This project aims to automatically identify images that contain ships using advanced machine learning techniques. By analysing satellite images, we can attempt to determine the presence of ships, which has applications in maritime safety, traffic monitoring, and environmental studies. We use a technique known as deep learning, which allows the computer to recognize patterns and features in images that are more likely to inidicate the presence of ships.

## Data
The model is trained on the Airbus Ship Detection Dataset, which contains satellite images of ships. This dataset is publicly available and is often used for object detection challenges in the machine learning community. Each image is labeled to indicate whether or not it contains a ship, allowing the model to learn from these examples.

See datasheet for more information: https://github.com/rifairbairn/ShipDetection/blob/main/Datasheet.md
Source: Airbus Ship Detection Challenge on Kaggle (https://www.kaggle.com/competitions/airbus-ship-detection)

## Model
We utilize the ResNet50 model, a powerful deep neural network known for its effectiveness in image classification tasks. ResNet50 is chosen for its deep architecture and ability to learn rich feature representations for complex visual tasks. The model has been pre-trained on a large dataset (ImageNet) and fine-tuned on our specific ship detection dataset to tailor its capabilities to our needs.

## Hyperparameter Optimisation
Due to the length of time taken to train the model, we only tried a handful of different hyperparameters. Testing different learning rates, dropout rates and batch sizes. Given less time constraints we would have liked to use Bayesian Optimisation to find the best set of hperparameters. 

## Results
The model achieved approximately 95% accuracy in detecting ships in satellite images, demonstrating its effectiveness for this task. The results indicate that the model can reliably distinguish between images with and without ships, which is crucial for practical applications. Here are some visualizations of the model predictions:

![image](https://github.com/rifairbairn/ShipDetection/assets/77961773/e5e870b2-1e97-4d04-a8f1-795f77ccb368)

The higher recall (97%) versus precision (85%), indicates a slight tendency to predict that there are ships when the model is unsure. As the model was designed to find images that are likely to have ships, so that a second model could detect the number of ships in each image, this tendency is a positive. In this workflow the cost of missing a ship is high, therefore the fact that the model rarely misses a ship (low False Negative rate) is a strength.

An investigation of the missclassified images suggests methods for dealing with particular weather features (glare, waves and clouds) would probably help to improve the model. 

Examples of two false negatives with glare:
![image](https://github.com/rifairbairn/ShipDetection/assets/77961773/2be70f71-d185-44fe-8bca-7d572488f8b4)

Examples of two false positives with difficult features:
![image](https://github.com/rifairbairn/ShipDetection/assets/77961773/57434f2c-bb8c-41eb-b4fc-bf35c6be7c58)
