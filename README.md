# Semantic Segmentation
###### SDC Term 3 Elective: Semantic Segmentation project

#### Project Overview

The main goal of this project was to study how works the Fully Convolutional Network (FCN) and main concepts like Decoder/Encoder, Transposed Convolution, Skip Connections and etc.
Here my dev.setup: Python 3.5.2, Tensorflow 1.4.0 and AWS g3.4xlarge with community AMI udacity-advanced-deeplearning. 
I experimented with several epochs values, batch sizes, learning rates and dropouts hyper parameters during training, and we finally settled on the following hyper parameters since the resulting model seems to generalize well and do not over or under fit the test data in the dataset:

* Epochs: 200
* Batch Size: 24 (One 160x576 pixel RGB image)
* Learning rate: 0.0001
* Dropouts: 0.5

The training time: 2h 30m, loss = 0.009

#### Examples

The following give examples of the output of this Fully Convolutional Network for Semantic Segmentation:

![alt text](./examples/um_000003.png)

![alt text](./examples/um_000010.png)

![alt text](./examples/um_000014.png)

![alt text](./examples/umm_000014.png)

The following resources were very helpful:
* SDC slack channel!
* [DeepLab: Semantic Image Segmentation (How it works)](https://www.youtube.com/watch?v=b6jhopSMit8) 
* [Tensorflow Tutorial](http://cv-tricks.com/tensorflow-tutorial/training-convolutional-neural-network-for-image-classification/)


### Setup
##### Frameworks and Packages
Make sure you have the following is installed:
 - [Python 3](https://www.python.org/)
 - [TensorFlow](https://www.tensorflow.org/)
 - [NumPy](http://www.numpy.org/)
 - [SciPy](https://www.scipy.org/)
##### Dataset
Download the [Kitti Road dataset](http://www.cvlibs.net/datasets/kitti/eval_road.php) from [here](http://www.cvlibs.net/download.php?file=data_road.zip).  Extract the dataset in the `data` folder.  This will create the folder `data_road` with all the training a test images.

### Start
##### Implement
Implement the code in the `main.py` module indicated by the "TODO" comments.
The comments indicated with "OPTIONAL" tag are not required to complete.
##### Run
Run the following command to run the project:
```
python main.py
```
**Note** If running this in Jupyter Notebook system messages, such as those regarding test status, may appear in the terminal rather than the notebook.

### Submission
1. Ensure you've passed all the unit tests.
2. Ensure you pass all points on [the rubric](https://review.udacity.com/#!/rubrics/989/view).
3. Submit the following in a zip file.
 - `helper.py`
 - `main.py`
 - `project_tests.py`
 - Newest inference images from `runs` folder  (**all images from the most recent run**)
 