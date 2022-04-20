# Melanoma Detection Using CNN
> Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution which can evaluate images and alert the dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.The purpose is to build a CNN based model which can accurately detect melanoma. 




## Table of Contents
* [General Info](#general-information)
* [Business Goals](#business-goals)
* [Model Building](#model-building)
* [Dataset](#dataset)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution which can evaluate images and alert the dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.The purpose is to build a CNN based model which can accurately detect melanoma. The model being built is a multiclass classification model using a custom convolutional neural network in TensorFlow.

The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.
The data set contains the following diseases:
1. Actinic keratosis
2. Basal cell carcinoma
3. Dermatofibroma
4. Melanoma
5. Nevus
6. Pigmented benign keratosis
7. Seborrheic keratosis
8. Squamous cell carcinoma
9. Vascular lesion



## Business Goals
The purpose is to build a CNN based model which can accurately detect melanoma. The model being built is a multiclass classification model using a custom convolutional neural network in TensorFlow.



## Model Building
1. Data Reading/Data Understanding → Defining the path for train and test images 
2. Dataset Creation→ Create train & validation dataset from the train directory with a batch size of 32. Also, make sure you resize your images to 180*180.
3. Dataset visualisation → Create a code to visualize one instance of all the nine classes present in the dataset 
4. Model Building & training : 
    a. Create a CNN model, which can accurately detect 9 classes present in the dataset. 
    b. While building the model, rescale images to normalize pixel values between (0,1).
    c. Choose an appropriate optimiser and loss function for model training
    d. Train the model for ~20 epochs
    e. Check if there is any evidence of model overfit or underfit.
5. Chose an appropriate data augmentation strategy to resolve underfitting/overfitting 
6. Model Building & training on the augmented data :
    a. Choose data augmentation technique to address issues of underfit\overfit in previous model.
    b. Train the model for ~20 epochs
    c. Check if the earlier issue is resolved or not.
7. Class distribution: Examine the current class distribution in the training dataset 
    a. Which class has the least number of samples?
    b. Which classes dominate the data in terms of the proportionate number of samples?
8. Handling class imbalances: Rectify class imbalances present in the training dataset with Augmentor library.
9. Model Building & training on the rectified class imbalance data :
    a. Check for Class Imbalance and apply Class Rebalancing technique to address Class imbalance
    b. Train the model for ~30 epochs
    c. Check if the earlier issue is resolved or not and impact on model performance.



## Dataset
The dataset is available in the google drive.
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.
The data set contains the following diseases:
1. Actinic keratosis
2. Basal cell carcinoma
3. Dermatofibroma
4. Melanoma
5. Nevus
6. Pigmented benign keratosis
7. Seborrheic keratosis
8. Squamous cell carcinoma
9. Vascular lesion



## Conclusions
- The class rebalance in the final model helped in reducing overfititng of the data and thus the loss is reduced. It also enhanced the overall accuracy of the model.
- Initially we tried building model without the ImageDataGenerator which created data to highly overfit.
- Then we introduced dropout to address overfitting and ImageDataGenerator for data augmentation which reduced the over fit, but significantly reduced the overall accuracy as well.
- At last we tried Batch Normalization and Augumentation which really helped in carry forward



## Technologies Used
pandas
numpy
matplotlib
tensorflow
keras
augmentor



## Acknowledgements
Sugandha Saurabh | github - @sugandhasaurabh


## Contact
Created by Sugandha Saurabh | github - @sugandhasaurabh



