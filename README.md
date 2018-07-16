# CarND Object Detection Lab

![](assets/clip.gif)

In lab this you will:

* Learn about *MobileNets* and separable depthwise convolutions.
* The SSD (Single Shot Detection) architecture used for object detection
* Use pretrained TensorFlow object detection inference models to detect objects
* Use different architectures and weigh the tradeoffs.
* Apply an object detection pipeline to a video.

Open the notebook and work through it!

### Download Models

Download the required modesl from the following location.

[Tensorflow Model Download](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/detection_model_zoo.md)

Download the models using the following commands.

```sh
wget http://download.tensorflow.org/models/object_detection/ssd_mobilenet_v1_coco_2018_01_28.tar.gz
wget http://download.tensorflow.org/models/object_detection/rfcn_resnet101_coco_2018_01_28.tar.gz
wget http://download.tensorflow.org/models/object_detection/faster_rcnn_inception_resnet_v2_atrous_coco_2018_01_28.tar.gz
  299  ls
```

After downloading the tarballs, untar in the appropriate directory.

### Requirements

Install environment with [Anaconda](https://www.continuum.io/downloads):

```sh
conda env create -f environment.yml
```

Change TensorFlow pip installation from `tensorflow-gpu` to `tensorflow` if you don't have a GPU available.

The environment should be listed via `conda info --envs`:

```sh
# conda environments:
#
carnd-advdl-odlab        /usr/local/anaconda3/envs/carnd-advdl-odlab
root                  *  /usr/local/anaconda3
```

Further documentation on [working with Anaconda environments](https://conda.io/docs/using/envs.html#managing-environments). 

Particularly useful sections:

https://conda.io/docs/using/envs.html#change-environments-activate-deactivate
https://conda.io/docs/using/envs.html#remove-an-environment


### Running on AWS.

Use the AWS provided Deep Learning AMI.

First activate the required environment among the various choices.
I used **tensorflow_p36**.

I issued the following command at the prompt.

```sh
source activate tensorflow_p36
```

I then installed moviepy and upgraded numpy.

Alternatively install a new environment using the environment file **aws_env.yml**

This can be done using the following command

```sh
conda env create -f aws_env.yml
```


### Resources

* TensorFlow object detection [model zoo](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/detection_model_zoo.md)
* [Driving video](https://s3-us-west-1.amazonaws.com/udacity-selfdrivingcar/advanced_deep_learning/driving.mp4)

### Tips
- Some windows users have reported the driving video as playable only in Jupyter Notebook operating in Chrome browser, and not in media player or Jupyter Notebook operating in other browsers.  In contrast the post-segmentation video appears to be operating accross players and browsers.
