Requirements:<br>Python 3.6<br> Tensorflow 1.3.0<br> Keras 2.0.7<br> Matplotlib latest!<br>

**1 Introduction** <br>
Adequate training of neural networks requires a lot of data. In the case of low data regime,
which is the case with most of the problems today, the existing networks generalize poorly.
To make progress on this foundational problem, we have decided to follow a low-shot
learning technique by exploiting the method of aggressive data augmentation and transfer
learning.<br>
**1.1 Related work**<br>
*One-shot and low-shot learning.* One class of approaches to one-shot learning uses generative models of appearance that tap into a global or a supercategory level prior. Generative
models based on strokes or parts have shown promise in restricted domains such as handwritten characters . They also work well in data-sets without much intra-class variation or
clutter.<br>
*Zero-shot learning.* Zero-shot recognition uses textual or attribute-level descriptions of
object classes to train classifiers. While this problem is different than ours, the motivation is
the same: to reduce the amount of data required to learn classifiers. One line of work uses
hand-designed attribute descriptions that are provided to the system for the novel categories.
Transfer learning. The ability to learn novel classes quickly is one of the main motivations
for multitask and transfer learning. Thrun‘’s classic paper convincingly argues that ““learning the n-th task should be easier than learning the first“”, with ease referring to sample
complexity. However, recent transfer learning research has mostly focused on the scenario
where large amounts of training data are available for novel classes. For that situation, the
efficacy of pre-trained ConvNets for extracting features is well known. There is also some
analysis on what aspects of ImageNet training aid this transfer.[1]<br>
*Data Augmentation.* The field of data augmentation is not new, and in fact, various data
augmentation techniques have been applied to specific problems. The main techniques fall
under the category of data warping, which is an approach which seeks to directly augment
the input data to the model in data space. The idea can be traced back to augmentation
performed on the MNIST set in [2].<br>
A very generic and accepted current practice for augmenting image data is to perform
geometric and color augmentations, such as reflecting the image, cropping and translating
the image, and changing the color palette of the image. All of the transformation are affine
transformation of the original image that take the form:<br>
y = W x + b<br>
The idea has been carried further in [3], where an error rate of 0.35% was achieved by
generating new training samples using data augmentation techniques at each layer of a deep
network. Specifically, digit data was augmented with elastic deformations, in addition to
the typical affine transformation. Furthermore, data augmentation has found applicability in
areas outside simply creating more data.<br>
**1.2 Problem, Goal, and Approach**
Current recognition systems require days or even weeks of training on expensive hardware to
develop good feature representations. The trained recognition systems may then be deployed
as a service to be used by downstream applications. These downstream applications may
need the ability to recognize new categories, but they may have neither the training data
required nor the infrastructure needed to retrain the models. Thus, there are two natural
phases: in the first phase, we have the data and resources to train sophisticated feature
extractors on large labeled datasets, and in the second phase, we want to add additional
categories to our repertoire at minimal computational and data cost.<br>
We are following the second phase. Our goal is to predict with high accuracy on a new
class for which we have very few examples. Instead of collecting new data which would
be both costly and time-consuming. Our approach is to use data augmentation and transfer
learning to make more data for novel class, as well, as saving time by not training the whole
model and using what the model already learned to extract basic features.<br>
We are using aggressive data augmentation which uses various transformations like
Coarse Dropout, Noise Embedding, Blur, Perspective Transformation, etc. and VGG16
model pre-trained on the ImageNet1K dataset for transfer learning.<br>

**To Read the whole Paper see the document below**
 [[Project Paper](https://github.com/ksw25/Deep-Learning/blob/master/Deep%20learning%20project/Project%20report%20deeplearning.pdf)]
