
Training The Model
====================

Dataset
========

A small dataset was used to train an automl model on predictions of flower types. 
The dataset, published on Kaggle, consisted of 250 images of flowers of 10 different 
categories. Before the model could be trained, the image dataset had to be properly 
structured. All of the images needed to be set up into the proper folder
according to their label. The dataset folder was compressed into a zip-file,
and uploaded into the Firebase Console Project database.   

The dataset file directory  structure is as follows:

<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
##The training dataset structure

flower-trainingset.zip
  |____0-phlox
  | |____001.png
  | |____002.png
  | |____003.png
  |____1-rose
  | |____010.png
  | |____012.png
  |____2-calendula
    |____025.png
    |____027.png
    |____030.png
  |..................
	|.........
	|.........
	|.........

</div>

</div> 
'''

Model Training
================

The AutoML Vision Edge API model, was run on a dataset directly from my android device. 
Using the Firebase Console, the model was trained, and then tested with 
images that were not included in the original dataset. I used images of flowers 
planted around my house, capturing the photos directly from my device camera, through
the Auto Ml Vision Edge API.  

Results...

The confusion matrix from the training dataset shows the model predicting most 
flowers label/type accurately. The model only experienced "confusion" 
while predicting labels for two categories of flowers (phlox and peony). When the model
was tested on images taken directly from my android device, many of the predictions 
were split amongst multiple labels. There was no image that had a predicted label
of 50% or more. 

This can be due to the amount of images in the original dataset, 
and the types of flowers in the dataset compared to those that were captured 
through my android device. Using a small dataset for training, such as the one used for this 
project which only consisted of 250 images, can negatively impact the precision of the 
models predictions on new data. The variety of image (flower) representations in this 
case could have also played a part in the models ability to accurately predict
the types of flowers in new images. The more representations a model has to work with
during training, the better its performance when tested on new data that it has not
yet been introduced to. 
