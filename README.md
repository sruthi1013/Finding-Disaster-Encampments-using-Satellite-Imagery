# Finding Tents and Other Emergency Housing Through Exploitation of Satellite Imagery

## Problem Statement
During disasters, emergency management agencies and humanitarian organizations need to know where survivors are congregating in order to provide emergency supplies and services. 


## Objectives
Create an app that can automate the process of rapidly identifying informal tent shelters erected by communities immediately following a natural disaster.

This project demonstrates a technical implementation of Step 1) of our objectives below, and outlines a practical approach to tackling the next steps objective 2) and 3).
Train a model to identify areas of damage surrounding a natural disaster. (completed)
Next Steps: Train another model to identify tent encampments in satellite imagery. (See Additional Resources for Next Steps.)
Next Steps: Use the locations of areas with damage as starting locations for an app that automatically scans the surrounding areas and identifies and alerts users of the whereabouts of any tent encampments (See Additional Resources for Next Steps.)


## Description of Data
Data was acquired from https://www.kaggle.com/kmader/satellite-images-of-hurricane-damage and consists of a training set of jpegs with 5000 images of each class (damage or no damage), and a test set with 1000 images of each class. Possible data for training the subsequent model that detects tents can be found in the Additional Resources below.


## Primary Findings/Conclusions
In this project, we have created a convolutional neural network model in python with TensorFlow and Keras tools that classifies a set of image data from Hurricane Harvey as either showing damage or not. This model worked with 95% test accuracy. It is specific to flood damage in a specific geography, but different datasets can be used to train a similar model to detect other types of damage in other geographies. In a final implementation, this model would be used on a dataset containing image geo-location data, and those locations where damage was identified will be used as starting locations for scanning the greater area for tent encampment detection.

Please refer to the Google Slides below for more information and recommendations for proceeding with this project: https://docs.google.com/presentation/d/1h3f5naFtOA5NTGIRI89voAw2l63D5ExxRtZBn6JectQ/edit?usp=sharing


## Additional Resources for Next Steps:

Tools/Resources for using Google Earth Engine for viewing and processing satellite data
Google Colab (like a jupyter notebook) is a relatively easy way to interface with Google Earth Engine using Python. (There is also a more widely used Javascript API with a GUI.)
Google Earth Pro (download, free) can be used to just explore satellite imagery, and peek at images at different points in history
Good intro to interfacing with Google Earth Engine with Python through Google Colab: https://youtu.be/IGUYSeoeHhg
Information for Google Earth Engine with Python: https://developers.google.com/earth-engine/python_install.html

### Modeling 
Using Tensor Flow in Google Colab:
https://github.com/google/earthengine-api/blob/master/python/examples/ipynb/TF_demo1_keras.ipynb

### Size of Encampments
Two papers are linked below on using segmentation and other techniques to detect/quantify tents in refugee camps. Although the context is different, these could be helpful in demonstrating techniques for next steps of this project for functionality to quantify the changing size of tent encampments: https://www.researchgate.net/publication/281490339_AUTOMATED_DETECTION_OF_REFUGEEIDP_TENTS_FROM_SATELLITE_IMAGERY_USING_TWO-LEVEL_GRAPH_CUT_SEGMENTATION
https://www.researchgate.net/publication/270455774_Detecting_tents_to_estimate_the_displaced_populations_for_post-disaster_relief_using_high_resolution_satellite_imagery

### Data and Labelling for tent detection model
MapSwipe (OpenStreetMap)
OpenStreetMap has a project called Missing Maps. Users can download the MapSwipe app to participate in labelling satellite images for a variety of projects. Projects include things like mapping refugee camps, mapping rural communities that might be prone to natural disaster or that need to be identified in order to prevent malaria. There are potentially useful datasets for training a model, or MapSwipe could possibly host a dataset to be labelled for a good cause.
Link to data: https://mapswipe.org/data.html

### Xview dataset
The below was found but not explored, and could contain the necessary data for training a tent detection model:
“ Defense Innovation Unit Experimental (DIUx) and the National Geospatial-Intelligence Agency (NGA) are releasing a new satellite imagery dataset to advance key frontiers in computer vision and develop new solutions for national security and disaster response.” http://xviewdataset.org/#dataset

