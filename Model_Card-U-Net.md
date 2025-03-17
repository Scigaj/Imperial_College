Model Card: U-Net with MobileNetV2 Backbone for Aerial Semantic Segmentation

Overview

This model is a U-Net architecture utilizing a MobileNetV2 backbone pre-trained on ImageNet. It has been fine-tuned for the task of semantic segmentation on aerial images captured by drones. The model is configured to classify each pixel into one of 23 distinct classes, making it suitable for detailed scene understanding in aerial imagery.

Model Details

Architecture: U-Net
Backbone: MobileNetV2
Encoder Weights: Pre-trained on ImageNet
Number of Classes: 23
Encoder Depth: 5
Decoder Channels: [256, 128, 64, 32, 16]
Activation: None (raw logits are produced, typically combined with a softmax during evaluation)
Training Data

Dataset: Aerial Semantic Segmentation Drone Dataset
Image Source: Drone-captured imagery
Annotations: Each image is paired with a corresponding semantic segmentation mask where pixel values represent different classes.
Preprocessing:
Images and masks are resized to a common dimension (704x1056) before augmentation.
Data augmentation includes horizontal and vertical flips, grid distortion, random brightness/contrast adjustments, and Gaussian noise.
Splits: The dataset is split into training, validation, and test sets.
Training Details

Loss Function: Cross-Entropy Loss
Optimizer: AdamW
Learning Rate Scheduler: OneCycleLR
Normalization:
Mean: [0.485, 0.456, 0.406]
Std: [0.229, 0.224, 0.225]
Batch Size: 3
Training Epochs: The model was trained over 15 epochs with early stopping based on validation loss.
Evaluation Metrics

Pixel Accuracy: Measures the ratio of correctly classified pixels to the total number of pixels.
Mean Intersection over Union (mIoU): Computes the average intersection over union across all classes, providing a robust measure of segmentation performance.
Intended Use Cases

Aerial Mapping: Detailed segmentation of aerial images for urban planning, agriculture, and environmental monitoring.
Disaster Response: Rapid scene analysis to identify damaged infrastructure.
Autonomous Navigation: Assisting in the navigation of drones in complex environments.
Limitations and Risks

Dataset Bias: The model is trained on a specific aerial dataset and may not generalize well to other domains or geographical areas without fine-tuning.
Resolution Constraints: Performance might be affected by the resolution of input images if they differ significantly from the training set.
Computational Requirements: Although MobileNetV2 is relatively lightweight, the overall U-Net architecture might still require a capable GPU for real-time inference.
Error Propagation: Misclassifications in segmentation can have cascading effects in downstream tasks (e.g., autonomous navigation).
Ethical Considerations

Privacy: Ensure that drone imagery is captured and used in compliance with privacy regulations.
Bias: Validate the model across diverse environments to mitigate potential biases in segmentation performance.
Deployment: Users should consider the implications of automated decision-making in critical applications such as disaster response or surveillance.
Contact and Further Information

For further details or inquiries regarding this model, please contact the development team or refer to the project documentation.
