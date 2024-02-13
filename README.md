# CNN based Melanoma Detection
> To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution which can evaluate images and alert the dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC)
- All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.
- The data set contains the following diseases:
  > Actinic keratosis
  > Basal cell carcinoma
  > Dermatofibroma
  > Melanoma
  > Nevus
  > Pigmented benign keratosis
  > Seborrheic keratosis
  > Squamous cell carcinoma
  > Vascular lesion

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
- A. With imbalanced data -
  1. Model.a: training_acc = 20%, validation_acc = 4% --> clear case of underfitting¶
  2. Model.b: training_acc = 98%, validation_acc = 34% --> clear case of overfitting
  3. Model.c: trianing_acc = 96%, validation_acc = 21% --> clear case of overfitting
  NOTE: Model.c has an additional dropout layer at the DNN layer. Validation accuracies differ by 13% which can be easily brought down/improved by playing around with dropout factors and adding additional dropout layers at ConvLayers
  4. Model.d: training_acc = training_acc = 89%, validation_acc = 30%
     NOTE: Model.d has more number of layers with intermediate dropout layers in the ConvLayers at one at the DNN. Some inference : Hence, it can be seen that Adding more layers with additional dropout layers does not improve the performance drastically BUT CERTAINLY TAKES LESSER TIME TO TRAIN!
- B. With Augmentation included - data balancing
     Model.d is used with augmented data
     training_acc = 90%, validation_acc = 84% --> This is pretty good. Problem of overfitting is solved

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- pathlib - version 1.0.1
- tensorflow - version 2.15.0
- pandas - version 1.5.3
- numpy - version 1.24.3
- pillow - version 10.2.0
- glob - version 0.7
- matplotlib - version 3.7.1
- Augmentor - version 0.2.12

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
- https://www.tensorflow.org/
- https://www.tensorflow.org/tutorials/images/classification#overfitting
- https://augmentor.readthedocs.io/en/master/


## Contact
Created by [@rk1989] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
