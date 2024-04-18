# Datasheet for the Airbus Ship Detection Dataset

## Motivation
Purpose: The Airbus Ship Detection Dataset was created to foster developments in the field of computer vision, specifically for the detection of ships in satellite images. This dataset supports tasks related to object detection, segmentation, and broad maritime activities like monitoring shipping lanes and maritime surveillance.
Creators and Funders: The dataset was created by Airbus for a competition hosted on Kaggle. Airbus is a corporation known for its aerospace products. The dataset's creation was likely funded internally as part of Airbus's initiatives to improve satellite image analysis.

## Composition
Data Instances: The dataset comprises satellite images that include various instances of ships. Images vary in terms of presence and absence of ships, as well as the number and size of ships.
Instance Count: The dataset contains approximately 190,000 labeled images, with approximately 65% containing no ships.
Missing Data: There are images in the referenced in the spreadsheet, that do not appear to be contained in the dataset. Approximately 230,000 images are detailed in the metadata spreadsheet.
Confidentiality: There is no confidential information as the images are satellite photos and do not include sensitive or personal data.

## Collection Process
Data Acquisition: The images are likely acquired from Airbus's satellites. Specific details on the satellites or sensors used are not typically disclosed in the dataset documentation.
Sampling Strategy: The dataset is a sample of Airbus’s comprehensive satellite imagery data. The specific strategy for selecting these particular images might involve scenarios with higher probabilities of ship presence.
Collection Time Frame: The exact time frame over which the images were collected is not specified.

## Preprocessing/cleaning/labelling
Preprocessing Steps: The images were preprocessed by Airbus, including labeling the ships' locations in the images using segmentation masks.
Raw Data: Only the processed images with annotations are provided in the dataset for use in the competition.

## Uses
Alternative Uses: Beyond ship detection, the dataset can be used for training models to recognize other objects in satellite images, monitor global shipping lanes, detect geographical changes over time, and environmental monitoring.
Impact and Risks: Care must be taken when using the dataset to avoid biases in model training, particularly in recognizing ships of varying sizes and under different weather conditions. Future users should be aware of the potential for models trained on this dataset to generalize poorly to different regions or conditions not well-represented in the data.
Prohibited Uses: The dataset should not be used for any navigational or operational decisions without further validation due to potential inaccuracies in the data.

## Distribution
Distribution: The dataset has been distributed primarily through Kaggle as part of a competition.
Copyright/IP License: The images are likely copyrighted by Airbus. The dataset is available under specific terms of use stipulated by Kaggle and Airbus for educational and research purposes, but not commercial use.

## Maintenance
Maintenance and Updates: The dataset is maintained by Kaggle and Airbus, with updates unlikely unless a new competition or project phase is announced.
