# DeeplearningUtils

This repository contains a collection of utilities useful in Deeplearning projects on tensorflow-keras platform. Utilities are arranged under 4 directories namely data, loss, model, optim_scheduler. Some of the utilities have been adapted from  other sources and they have been acknowledged.
The utilities are summarised below.

## Data

This directory contains modules related data preprocessing and augmentation eg. normalization, padding, cutout etc.
Various modules in this directory are listed below.

Included modules
* data_augment_utils.py
  * get_random_eraser

     Returns a function to apply random cutouts on a batch of data. The function allows user to configure probability of cutout, its aspect ratios, max and min area etc. This function has been adapted from [here](https://github.com/yu4u/cutout-random-erasing) to work with tensorflow tf.data.datset.map() method. 

* data_preProcess_utils.py
  * data_preProcess
  
    It applies normaization to input training and test data using training data mean and std. Data are then padded with 4 pixels.

* tf_record_utils.py
  * save_tf_records
  
    It converts input data into tf_record format and stores it at provided path.
  
  * load_tf_records_as_dataset
  
    It loads data stored at given path in tf_record format and decodes it to return data as tf.data.dataset. 
  
  
## Model

This directory contains modules related to model definitions and related helper functions. It also contains utilities for visualization of model training and testing

Included modules
* model_defn_utils.py
  * DavidNet
  
    It defines one of the models submitted for [DAWNBench](https://dawn.cs.stanford.edu/benchmark/index.html#cifar10) competition by David C. Page. It is a custom built 9-Layer ResNet model. More details can be found [here](https://mc.ai/tutorial-2-94-accuracy-on-cifar10-in-2-minutes/).
  
* model_log_plot_utils.py
  * model_log_plot
  
    It plots given train and test accuracy and loss data side-by-side
