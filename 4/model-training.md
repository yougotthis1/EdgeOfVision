Training The Model
====================
Dataset

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
```
</div>

</div> 

Model Training

Below are screemshots of the AutoML Vision Edge API model, which was
run on a dataset directly from my android device. Using the Firebase Console,
the model was trained, and then tested with images that were not included in the 
original dataset. I used images of flowers planted around my house, capturing
the photos directly from my device camera, through the Auto Ml Vision Edge API.
Below are screenshots of the trained-data and test-data screens on the app. 
![Firebase Console Auto ML - Model Training](../../../images/edge_trained.jpg),
(../../../images/edge_test.jpg)

Results...

The confusion matrix from the training dataset shows the model predicting most 
flowers label/type accuratley. The model only experienced "confusion" 
while predicting labels for two categories of flowers (phlox and peony). When the model
was tested on images teken directly from my android device, many of the predictions 
were split amongst mutiple labels. There was no image that had a predicted label
of 50% or more. This can be due to the amount of images in the original dataset, 
and the types of flowers in the dataset compared to those that were captured 
through my android device.  
