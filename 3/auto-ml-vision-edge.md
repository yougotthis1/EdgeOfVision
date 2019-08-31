---
title: 'Auto ML Vision Edge'
prev_page:
  url: /1/2/firebase.html
  title: 'Firebase Setup'
next_page:
  url: /1/4/model-training.html
  title: 'Prediction Model Training on Android Device'
title: 'Auto ML Vision Edge API'

prev_page:

  url: /1/2/firebase.html

  title: 'Firebase Setup'

next_page:

  url: /1/4/model-training.html

  title: 'Prediction Model Training on Android Device'

comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"

comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---
Auto ML Vision Edge 
====================

The last important piece needed before the model can be trained, is Auto ML. 
Since this project focuses on running machine learning models on the edge, 
Auto ML Vision Edge is the API specifically used. It is one of ML Kits base-on-device
image labeling API models. It trains models based on data uploaded into the projects
database via the Firebase Console. Similar to the other dependencis, the sdk file 
must be added to the applications build.gradle file. 
![Firebase Console Auto ML Android Project](../../images/project_home.jpg), 
(../../../images/project_home2.jpg)

Once the initial model is trained, the models performace can be evaluated, 
and a number of measures are provided, including a confusion matrix. 
After evaluting the model, it can be tested with new images. The images can be both captured 
and uploaded directly from the edge device (android phone in this case). The model can then 
be run on the new images, provding its predictions generated on the new images.

![Firebase Console Auto ML - Model Training](../../../images/confusion-matrix.jpg)



