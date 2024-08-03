# xray-image-recognition
**Xray image recognition project**

This project involves the analysis of chest X-ray images to
detect COVID-19 cases.

**Pre-processing Steps**

    ● Images were resized to 224x224 pixels to maintain consistency.
    
    ● Data augmentation techniques such as random horizontal and
    vertical flips, rotations up to 15 degrees, and random crops with
    padding were employed to enhance the dataset's variability and
    improve model generalization.
    
    ● Color adjustments were made through transformations like
    brightness, contrast, saturation, and hue modifications to better
    simulate different lighting conditions.
    
    ● Normalization was applied to the images with specific means and
    standard deviations to standardize the data across the dataset.

**Developed Models**

**CNN**

    ● The model includes several convolutional layers responsible for
    feature extraction from the images. Each layer uses different filters
    to detect specific features in the data.
    
    ● Following the convolutional layers are pooling layers, which help
    reduce data dimensionality while preserving important features.
    
    ● Fully connected layers are used for image classification based on the
    extracted features.



**Pretrained RestNet**

    ● Adapted ResNet18 model with pretrained weights is used. 
    
    ● The main layer of the model (fc layer) has been
    modified to match the number of classes in our task.
    
    ● Regularization and normalization layers (Dropout, BatchNorm) have been added.

**Key Findings**

    ● The CNN model demonstrated superior performance with high accuracy, precision, recall, and F1 scores. It showed
    robustness in handling fluctuations in training and validation losses, indicating strong generalization capabilities.
    
    ● The ResNet model, while effective, highlighted areas for improvement, particularly in handling higher validation losses
    which suggest potential overfitting.
    
    ● Early stopping implemented in training both models prevented overfitting and unnecessary computations by halting
    training when no significant improvement in validation loss was observed.
