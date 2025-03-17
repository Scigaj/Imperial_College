# Imperial_College

### **SEMANTIC SEGMENTATION PORTFOLIO PROJECT**

**What is Semantic Segmentation?**

Semantic segmentation is an advanced computer vision technique that involves partitioning an image into distinct, semantically meaningful regions, where every pixel is classified into a specific object category. Unlike traditional image classification or object detection, which might only identify the presence of an object or provide bounding boxes, semantic segmentation assigns a label to each individual pixel, effectively “understanding” the image at a granular level.

At its core, semantic segmentation aims to provide a comprehensive understanding of the scene by differentiating between various objects and backgrounds. For example, in an autonomous driving scenario, a semantic segmentation system can distinguish roads, vehicles, pedestrians, trees, and buildings from one another. This pixel-level classification is critical for decision-making systems that require precise localization of objects in real time.

Deep learning, particularly convolutional neural networks (CNNs), has revolutionized the field of semantic segmentation. Architectures like Fully Convolutional Networks (FCNs) replaced traditional fully connected layers with convolutional layers to maintain spatial information, making them suitable for pixel-wise predictions. Later innovations, including models like U-Net, DeepLab, and SegNet, have introduced enhancements such as encoder-decoder frameworks and dilated convolutions. These improvements help capture both high-level context and fine-grained details by considering various scales of features without sacrificing resolution.

The training process for semantic segmentation models often relies on large, meticulously labeled datasets where every pixel is annotated. This pixel-level annotation is resource-intensive, prompting ongoing research into more efficient, weakly-supervised, and unsupervised methods to reduce the reliance on extensive manual labeling.

In summary, semantic segmentation is fundamental for applications requiring detailed scene understanding. By providing a comprehensive pixel-wise classification of images, it enables systems across various domains—from autonomous vehicles to medical imaging—to make informed and precise decisions based on complex visual inputs.


### **DATA SET**

**Aerial Semantic Segmentation Drone Dataset**

**About Dataset**

Dataset Resource: https://www.tugraz.at/index.php?id=22387

Citation

If you use this dataset in your research, please cite the following URL:

http://dronedataset.icg.tugraz.at

License
The Drone Dataset is made freely available to academic and non-academic entities for non-commercial purposes such as academic research, teaching, scientific publications, or personal experimentation. Permission is granted to use the data given that you agree:

That the dataset comes "AS IS", without express or implied warranty. Although every effort has been made to ensure accuracy, we (Graz University of Technology) do not accept any responsibility for errors or omissions.
That you include a reference to the Semantic Drone Dataset in any work that makes use of the dataset. For research papers or other media link to the Semantic Drone Dataset webpage.
That you do not distribute this dataset or modified versions. It is permissible to distribute derivative works in as far as they are abstract representations of this dataset (such as models trained on it or additional annotations that do not directly include any of our data) and do not allow to recover the dataset or something similar in character.
That you may not use the dataset or any derivative work for commercial purposes as, for example, licensing or selling the data, or using the data with a purpose to procure a commercial gain.
That all rights not expressly granted to you are reserved by us (Graz University of Technology).

Dataset Overview
The Semantic Drone Dataset focuses on semantic understanding of urban scenes for increasing the safety of autonomous drone flight and landing procedures. The imagery depicts more than 20 houses from nadir (bird's eye) view acquired at an altitude of 5 to 30 meters above ground. A high resolution camera was used to acquire images at a size of 6000x4000px (24Mpx). The training set contains 400 publicly available images and the test set is made up of 200 private images.

PERSON DETECTION
For the task of person detection the dataset contains bounding box annotations of the training and test set.

SEMANTIC SEGMENTATION
We prepared pixel-accurate annotation for the same training and test set. The complexity of the dataset is limited to 20 classes as listed in the following table.

Table 1: Semanic classes of the Drone Dataset

tree, gras, other vegetation, dirt, gravel, rocks, water, paved area, pool, person, dog, car, bicycle, roof, wall, fence, fence-pole, window, door, obstacle
