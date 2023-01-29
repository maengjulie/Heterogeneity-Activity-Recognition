# Heterogeneity-Activity-Recognition
Evaluating Deep Learning Models with Smartphone Sensor Data\
*w/ Hyunbin Kim*
* Background
  * IoT technologies are integrated in smartphones and smartwatches
  * Sensors can monitor physical activities → Human Activity Recognition (HAR)
  * Priority lies in evaluating sensors
  * Aims to explore the performance of accelerometer through deep learning model
* Data: UCI HAR Dataset
  * Test subjects: 30 volunteers aged between 19 and 48
  * Samsung Galaxy smartphone
  * 6 kinds of activities: Walking, Walking Upstairs, Walking Downstairs, Sitting, Standing, Laying
  * 50 accelerations of coordinates x, y, z per second
  * Pre-processed with noise filters
  * 128 readings per window
* Experiment with 5 types of RNN LSTM models
  * Different types of layers for each model
  * Epochs = 50, batch size = 64 fixed
* Focusing on minimizing fluctuations and gaps between training and validation curves:
  * LSTM itself has good performance
  * Model with Conv1D layer has best fit for our HAR data
  * GRU does not work efficiently with large data
