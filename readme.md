# Deep Video Analytics

by [Akshay Bhat, Cornell University.](http://www.akshaybhat.com)  [![Build Status](https://travis-ci.org/AKSHAYUBHAT/DeepVideoAnalytics.svg?branch=master)](https://travis-ci.org/AKSHAYUBHAT/DeepVideoAnalytics)

![UI Screenshot](docs/figures/emma.png "Emma Watson, from poster of her latest subject appropriate movie The Circle")
![Banner](docs/figures/banner_small.png "banner")

Deep Video Analytics is a platform for indexing and extracting information from videos and images. For installation instructions & demo go to [https://www.deepvideoanalytics.com](https://www.deepvideoanalytics.com)
**Don't be worried by complexity of this banner, with latest version of docker installed correctly, you can run Deep Video Analytics in minutes locally (even without a GPU) using a single command.**

#### Documentation & tutorial

- For a quick overview we recommend going through the [presentation in readme.pdf](readme.pdf)

- Documentation along with a tutorial is being written in [/docs/tutorial](/docs/tutorial) directory.

#### Experiments

- ** OCR example has been moved to [/docs/experiments/ocr](/docs/experiments/ocr) directory**.

#### Deployment

We provide instructions for deploying DVA in three scenarios.

1. [deploy/cpu](/deploy/cpu) contains docker-compose files for non-GPU single machine deployments on Linode, AWS, GCP etc.

2. [deploy/gpu](/deploy/gpu) contains docker-compose files for GPU single machine deployments on AWS etc.

3. [deploy/gcp](/deploy/gcp) contains files used for launching DVA in a scalable GKE + GCS setup


#### Architecture, Data & Processing model

![Data model](docs/figures/data_model_2.png "data model")

![Processing model](docs/figures/task_model_2.png "processing model")

#### Code organization

- /client : Python client using DVA REST API
- /configs : ngnix config + defaults.py defining models + processing pipelines (can be replaced by mounting a volume)
- /deploy : Dockerfiles, compose files for single machine CPU/GPU deployment, scalable deployment with GCS & Kubernetes on GCP
- /docs : Documentation, tutorial and experiments
- /tests : Files required for testing
- /repos : Code copied from third party repos, e.g. Yahoo LOPQ, TF-CTPN etc.
- /server : dvalib + django server contains contains bulk of the code for UI, App and models.
- /logs : Empty dir for storing logs

#### Libraries modified in code and their licenses

| Library  | Link to the license | 
| -------- | ------------------- |
| YAD2K  |  [MIT License](https://github.com/allanzelener/YAD2K/blob/master/LICENSE)  |
| AdminLTE2  |  [MIT License](https://github.com/almasaeed2010/AdminLTE/blob/master/LICENSE) |
| FabricJS |  [MIT License](https://github.com/kangax/fabric.js/blob/master/LICENSE)  |
| Facenet   |  [MIT License](https://github.com/davidsandberg/facenet)  |
| JSFeat   |  [MIT License](https://inspirit.github.io/jsfeat/)  |
| MTCNN   |  [MIT License](https://github.com/kpzhang93/MTCNN_face_detection_alignment)  |
| CRNN.pytorch  |  [MIT License](https://github.com/meijieru/crnn.pytorch/blob/master/LICENSE.md)  |
| Original CRNN code by Baoguang Shi  |  [MIT License](https://github.com/bgshih/crnn) |
| Object Detector App using TF Object detection API |  [MIT License](https://github.com/datitran/Object-Detector-App) | 
| Plotly.js |  [MIT License](https://github.com/plotly/plotly.js/blob/master/LICENSE) | 
| CRF as RNN  |  [MIT License](https://github.com/sadeepj/crfasrnn_keras/blob/master/LICENSE) | 
| Text Detection CTPN  |  [MIT License](https://github.com/eragonruan/text-detection-ctpn/LICENSE) | 
| SphereFace  |  [MIT License](https://github.com/wy1iu/sphereface/blob/master/license) |
| Segment annotator  |   [BSD 3-clause](https://github.com/kyamagu/js-segment-annotator/blob/master/LICENSE) |
| TF Object detection API  | [Apache 2.0](https://github.com/tensorflow/models/tree/master/research/object_detection) |
| TF models/slim  | [Apache 2.0](https://github.com/tensorflow/models/tree/master/research/slim) |
| TF models/delf  | [Apache 2.0](https://github.com/tensorflow/models/tree/master/research/delf) |
| Youtube 8M feature extractor  | [Apache 2.0](https://github.com/google/youtube-8m) |
| CROW   |  [Apache 2.0](https://github.com/yahoo/crow/blob/master/LICENSE)  | 
| LOPQ   |  [Apache 2.0](https://github.com/yahoo/lopq/blob/master/LICENSE)  | 
| Open Images Pre-trained network  |  [Apache 2.0](https://github.com/openimages/dataset/blob/master/LICENSE) |


#### Additional libraries & frameworks

* FFmpeg (not linked, called via a Subprocess)
* Tensorflow 
* OpenCV
* Numpy
* Pytorch
* Docker
* Nvidia-docker
* Docker-compose
* All packages in [requirements.txt](/requirements.txt)
* All dependancies in [Dockerfile](/deploy/dockerfiles/Dockerfile)



# License & Copyright

**Copyright 2016-2017, Akshay Bhat, Cornell University, All rights reserved.**

# Contact

Deep Video Analytics is currently in active development.
The license will be relaxed once a stable release version is reached.
Please contact me for more information. For more information see [answer on this issue](https://github.com/AKSHAYUBHAT/DeepVideoAnalytics/issues/29)
 
