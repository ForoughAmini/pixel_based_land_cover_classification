# Pixel-Based Land Cover Classification
## Project Overview

This project develops a pixel-based land cover classification of Colorado Springs, USA, using a 2010 Landsat 5 TM Level-2 Surface Reflectance image. The workflow follows the Geographical Research Methods 1: Earth Observation practical on supervised land cover classification, with additional machine-learning experiments.

Six spectral bands were used as input features: Blue, Green, Red, NIR, SWIR 1 and SWIR 2. Four land-cover classes were considered:

Bare soil
Vegetation
Water
Urban area

Training samples were collected from representative areas of the different land-cover classes. The samples were inspected using their spatial distribution and spectral characteristics before being used for supervised classification. The data were divided into training and validation samples for model development and accuracy assessment.

## Classification Methods

The original practical workflow was extended by implementing and comparing several supervised machine-learning classifiers:

Nearest Centroid
Maximum Likelihood Classifier
K-Nearest Neighbors (KNN)
Multi-Layer Perceptron (MLP)
Decision Tree
Random Forest

For each classifier, the training and validation performance was evaluated using overall accuracy, Cohen's Kappa, and confusion matrices. Producer's Accuracy, User's Accuracy, omission error and commission error were also derived from the confusion matrices.

In addition to the baseline classifiers, GridSearchCV was used to investigate suitable hyperparameter combinations for each model. The selected models were subsequently evaluated on the same validation data and their classification maps were compared with the baseline results.

## Results

The baseline experiments showed differences in both quantitative performance and spatial classification patterns between the models. The baseline KNN and Random Forest models achieved the highest validation accuracies, while the different classifiers showed distinct patterns of confusion between land-cover classes. Water was generally classified very well, whereas urban areas showed substantially more confusion with other classes, particularly bare soil.

The classification maps also revealed differences that are not fully represented by overall accuracy. For example, some classifiers preserved narrow or spatially separated urban structures more clearly, while others produced more fragmented predictions.

Hyperparameter tuning did not lead to a consistent improvement for all classifiers. Some models showed improved validation performance, whereas others showed little improvement or a decrease in accuracy. This illustrates that model complexity and parameter tuning do not automatically result in better generalization for a given dataset. The spatial maps were therefore considered together with the quantitative accuracy measures when interpreting the results.

## Additional Analysis

The project also includes an inspection of the spectral characteristics and extreme values of the training samples. This was used to better understand the variability within the land-cover classes and the influence of the training data on classification performance.

Further analysis of the results focuses on the confusion matrices and class-specific accuracy measures, together with visual comparison of the resulting land-cover maps.

## Acknowledgement

The initial workflow and several coding concepts used in this project were learned from the Geographical Research Methods 1: Earth Observation course at Vrije Universiteit Brussel (VUB). The course practicals and accompanying code provided the foundation for the data preparation and classification workflow, which was subsequently adapted and extended for this project.