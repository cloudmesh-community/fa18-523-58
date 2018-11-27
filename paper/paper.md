# Caffe - The Deep Learning Framework :smiley: :exclamation: fa18-523-58

| Pramod Duvvuri
| vduvvuri@iu.edu
| Indiana University
| hid: fa18-523-58
| github: [:cloud:](https://github.com/cloudmesh-community/fa18-523-58/blob/master/paper/paper.md)

## Introduction

The amount of data generated has increased exponentially and so did the advancement of computing power, both these have led us to the era of deep learning. This paper aims to summarize a deep learning framework knows as Caffe [@hid-sp18-404-jia2014caffe] which was developed by a post-doctorate student *Yangqing Jia* at the University of California, Berkeley in 2013. It is written in C++ and is known for its fast execution and its Python interface allows it to be used by the vast majority of Python users. The framework has then been open-sourced, allowing many users to use, develop and contribute to improving the framework. The deep learning [@fa18-523-58-DL] revolution has led to the need for state-of-the-art implementations of Artificial Neural Network (ANN) architectures. These architectures are too hard to code from scratch for most people even with a conceptual understanding. The first deep learning framework to gain popularity was *Theano* [@www-theano]. Theano was developed at the University of Montreal in 2007. It was primarily used by academic researchers at the university. Theano was built using Python which essentially made it slower for larger models, for production-grade models speed is imperative. This meant there was a need for a new popular and fast deep learning framework, especially in computer vision. Caffe was built using C++ and this made it very fast and ideally suitable for deployment in production. Caffe [@www-caffe] at the time of public release or open sourcing had the best implementation of a Convolutional Neural Network [@fa18-523-58-cnn], which is primarily used in solving computer vision problems. This public release made all the computer vision researchers and other people in the computer vision community adopt Caffe.

---

Keywords: hid fa18-523-58, [Artifical Neural Network] (#Artificial-Neural-Network), C++, [Computer Vision] (#Computer-Vision), [Deep Learning] (#Deep-Learning), Machine Learning, Python

---

## Artifical Neural Network

Neural Network is a machine learning algorithm which mimics the human nervous system. It consists of various nodes or artificial neurons that are interconnected and perform machine learning tasks. The advancements in computation and the introduction of Graphical Processing Units [@fa18-523-58-GPU] (GPUs) have made it feasible for us to run such sophisticated algorithms. Neural networks have performed exceptionally well on data in comparison to other industry standard machine learning algorithms, which is why they have been adopted by both the academia and the industry. They require far more training data or examples than other algorithms and also require a considerable amount of computational resources to run.

## Computer Vision

Computer vision [@fa18-523-58-vision] primarily consists of computers trying to extract or understand meaningful information from images or videos from the real world. It is a vast field that consists of many domains under it. The main goal of computer vision is to build a system that can mimic the human vision or visualize an image and understand the context and semantics. The input for such a system can take multiple forms such as a single image, sequence of images or a video or multi-dimensional data. Some of the most common are object recognition, object tracking, image segmentation, image processing. The deep learning revolution has essentially revitalized the field of computer vision. Many problems which were considered impractical have been solved using deep learning. Artificial Intelligence [@fa18-523-58-AI] and Computer Vision have a lot of common topics. Quite a few of these problems such as pattern recognition in vision were solved with the help of artificial intelligence and this made computer vision an integral part of artificial intelligence.

## Deep Learning

Deep learning is a set of techniques or architectures that use Deep Neural Networks (DNNs) to solve problems in various fields such as computer vision, signal processing [@fa18-523-58-Sig-Processing], natural language processing [@fa18-523-58-NLP]. These DNNs can be used to solve any type of machine learning problem. Deep Neural Networks are Neural networks with more than two layers. There are usually two main types of in machine learning:

1. *Supervised Learning*: In supervised learning, the data used to train our machine learning model is categorized into various categories also known as labels. The model is trying to learn how to categorize our data into these categories.

2. *Unsupervised Learning*: In unsupervised learning, there are no categories. The algorithms are trying to find patterns or similarities in the data we give as input.

Any deep learning architecture at its core consists of a perceptron. A perceptron [@fa18-523-58-Perceptron] is a machine learning algorithm which was made to mimic the function of a human neuron. Deep learning architectures use multiple such perceptrons or nodes as layers which is the reason these are referred to as deep learning architectures. In computer vision problems each layer serves a specific purpose and the combination of all these layers aids in solving specific problems.

## Installation

To use Caffe it is recommended to install a containerized image of it. This can be done using the help of Docker [@www-docker-tutorial]. The official Caffe image can be found on DockerHub and can be installed using the GUI. It can also be installed using the following command with docker already running on your local machine. In your docker terminal please paste the following command:

```bash
docker run -ti bvlc/caffe:cpu caffe --version
```
```
caffe version 1.0.0
```
As indicated the latest version is 1.0.0, the above command is mostly used if the machine does not contain a GPU [@fa18-523-58-GPU]. If your machine contains a dedicated GPU then another command can be used to install Caffe using Docker. In your docker terminal please paste the following command:

```bash
nvidia-docker run -ti bvlc/caffe:gpu caffe --version
```
```
caffe version 1.0.0
```
With Caffe now installed it can be used with an Interactive Python notebook. The below command must be used to launch an IPython notebook in the docker terminal and then import caffe in the interactive Python (IPython) notebook [@www-jupyter-6] before we can write any code in Caffe.

```bash
docker run -ti bvlc/caffe:cpu ipython
import caffe
```


## Architecture

The Caffe architecture mainly consists of layers or it had a layer-wise design all designed and built from scratch using C++ and the CUDA [@www-cuda-wikipedia] architecture with various interfaces to write code in MATLAB [@fa18-523-58-MATLAB] and Python. This architecture at the time of its creation was considered really good but since then newer deep learning framework's such as *Tensorflow* which was created by Google has a much flexible design. This flexible design is with respect to the various nodes in the Artificial Neural Network [@fa18-523-58-ANN] (ANN) since ANNs primarily consist of layers and each layer has multiple nodes. The ability to flexibly design these nodes was very important to the researchers since this helped them achieve higher accuracy rates for their model and this helped with benchmarking and comparison with other similar models aimed to solve similar tasks.

## Applications

Some of industry grade production levels applications [@hid-sp18-404-Evan] of Caffe are:

* Facebook used Caffe to generate alternate texts who people who are visually challenged. All the photos uploaded to Facebook were run through a caffe model to generate such text. Facebook also used caffe to detect objectionable content. As the amount of data on social media increases so has the need for a protocol to regulate and report objectionable content risen.

* Pinterest used Caffe for object detection in the images. All the images that were uploaded were run through a model for object detection. The Caffe deep learning model for visual search could search over billions of images in just under 250 milliseconds. As many as 4 million images are uploaded onto Pinterest on a daily basis.

* Yahoo used Caffe for user recommendations in Japan. The news feed on Yahoo had stories curated using a caffe model and also made restaurant suggestion using photos. Yahoo also had models to automatically arrange photos of users into albums.

## Limitations and Comparisons

Caffe was developed by a post-doctorate student and then open sourced in 2013, the deep learning revolution had just begun when Caffe was launched. After its initial launch, there were more than 150 developers who were actively contributing to the framework. At the same time, large companies such as Amazon, Facebook, Google, Microsoft had all begun working on deep learning frameworks which suited their needs and fit perfectly in their respective technology stacks. The public launch of Tensorflow [@fa18-523-57-TensorFlow] by Google made a lot of people adopt it quickly since Google had consistently invested more time and money in the development and maintenance of this framework. Currently, there are more 1500 people who actively contribute to the Tensorflow framework. *PyTorch* [@fa18-523-57-PyTorch-Wikipedia] is another popular deep learning framework which was developed in 2017 at Facebook and had dynamic graph computational ability which was lacking in Tensorflow. PyTorch was received very well by the research community since it combines two of the most popular languages used by the artificial intelligence community Torch and Python. Caffe main strength was its implementation of a fast CNN [@fa18-523-58-cnn] and ready to use GPU [@fa18-523-58-GPU] support. Although CNNs could be used for Natural language processing [@fa18-523-58-NLP] (NLP) tasks there were other deep learning architectures which were more suitable for NLP related tasks. Other deep learning frameworks such as Theano and Torch had better implementations of these architectures hence they were preferred to Caffe. This meant that caffe's usability was very limited outside computer vision tasks. Caffe does not offer multi-GPU support. The exponential rise in our data meant we needed to use multiple powerful GPUs to train our models. Hence modern frameworks such as Tensorflow and PyTorch were built to serve as an all-purpose deep learning framework that had the state-of-the-art implementations of the latest deep learning architectures and also had out of the box multi-GPU support. Gradually people adopted these frameworks over Caffe. These frameworks had a much more robust architecture. Caffe was restricted by the format for input and output. It only supports one output format called HDF5 [@fa18-523-58-HDF5]. Caffe had less documentation and fewer hands-on tutorials which made it less developer friendly [@fa18-523-58-Quora-Answer-3].


## Conclusion

Caffe was mainly intended to support vision tasks and was not suitable for other tasks such as speech recognition, language modeling and time series data. This made its applications and also usability limited. But the lack of proper documentation and examples made it harder to adopt for the community. All modern deep learning frameworks were built to overcome the limitations of Caffe. They also borrowed its excellent CNN implementation. More people have since then moved to Tensorflow for academic research. Caffe has contributed a lot the computer vision and deep learning communities. Caffe helped these communities make valuable contributions to research with its fast execution times. Caffe2 [@fa18-523-58-Caffe2] was a project that was started at Facebook after the success of Caffe. Caffe2 was open sourced by Facebook in April 2017. By the end of March 2018, Caffe2 was merged with PyTorch by Facebook. These days the choice of a deep learning framework, when you have huge amounts of data, is either PyTorch or Tensorflow. Both Google and Facebook constantly keep updating these frameworks from the feedback they receive from the developer community to make it more developer friendly with the ability to visualize the computational graphs. The goal now is to make deep learning more accessible to everybody and reduce the steep learning curves when it comes to these deep learning frameworks and caffe has contributed invaluably to achieve this goal.
