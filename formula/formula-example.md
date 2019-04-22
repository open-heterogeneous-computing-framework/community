# Formula-0: Running Image Recognition Machine Learning Job On FPGA

## Scenario
User/admin could use the acceleration service provided by OpenStack Cyborg
project to program a FPGA card with an image developed for machine learning, and
then use that dynamically programmed FPGA card to accelerate the pre-trained
model serving for image recognition task.

## Components

### Hardware
#### General Computing Resource:

* Intel(R) Xeon(R) CPU E5-2670 0 @ 2.60GHz

#### Acceleration Resource:

* Intel® Programmable Acceleration Card with Intel® Arria® 10 GX FPGA

* Bitstream: optimized for ResNet model, size 88M

### Software
#### AI models
Upstream: [opencv modelzoo](https://github.com/opencv/open_model_zoo/):

* Face detector based on SqueezeNet light (half-channels) as a backbone with a
single SSD for indoor/outdoor scenes shot by a front-facing camera. The backbone
consists of fire modules to reduce the number of computations. The single SSD
head from 1/16 scale feature map has nine clustered prior boxes.

* Fully convolutional network for simultaneous Age/Gender recognition. The
network is able to recognize age of people in [18, 75] years old range, it is
not applicable for children since their faces were not in the training set
Head pose estimation network based on trimmed SqueezeNet_v1.1. Angle regression
layers are convolutions (width: 128) + ReLU + batch norm + fully connected with
one output

* Fully convolutional network for recognition of five emotions ('neutral',
'happy', 'sad', 'surprise', 'anger')

#### AI Framework:
Upstream:[Caffe](https://github.com/BVLC/caffe)

#### AI Inference Engine:
Upstream:[OpenVINO toolkit](https://github.com/opencv/dldt)

#### Cloud Platform:
Upstream:[OpenStack Cyborg](https://github.com/openstack/cyborg)

## PoC
### Recording
OpenStack Berlin Summit Keynote [Demo](https://www.youtube.com/watch?v=92dEEP1K5ZU&t=377s)

### Taskflow:
Glance image-list to show the available images
Cyborg acc-show to show the available accelerators
Cyborg acc-program to show the programming of a new image to the accelerator (FPGA)
Cyborg acc-show to show the newly changed accelerator with new image (metadata)
OpenVINO toolkit for model inference of an video of Obama walking with Joe Pedsta.

## Identified Gaps
### Gaps For Full Fledged Demo
* Due to the complexity of kubernetes DPI Plugin development for Intel A10 FPGA,
kubernetes and kubeflow were not used in the MVP version of the demo.

* Runs on bare metal since Nova integration not done in Rocky release, but VM
accessed programming should be of little difference.
### Gap Fulfillment
* OpenStack: ongoing - Nova/Cyborg integration
* Kubernetes: ongoing
