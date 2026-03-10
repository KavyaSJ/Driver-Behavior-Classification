# Driver-Behavior-Classification
Image  Classification using Neural Network

## Data Source:
https://www.kaggle.com/code/imtkaggleteam/driver-behavior-detection-cnn

## Objective:

The primary objective of this project is to develop a deep learning-based image classification model that can automatically detect and classify different driver behaviors. The system aims to distinguish between safe driving and various distracted behaviors such as texting, calling, or turning away from the road.

By leveraging Convolutional Neural Networks (CNNs) like VGG16, MobileNet and AlexNet, the model learns visual patterns associated with each behavior category. The goal is to achieve high classification accuracy and reliable real-time performance.

## Dataset:

The dataset consists of driver images categorized into five classes representing different driving behaviors.
#### classes:

- Safe Driving
- Texting on phone
- Talking on phone
- Turning
- Other Activities

## Dataset preprocessing included:

- Removing corrupted images
- Detecting duplicate images
- Normalizing pixel values
- Splitting data into training, validation, and test sets

## Models Implemented

The following deep learning models were implemented and compared:

### AlexNet

AlexNet is a deep learning model that made a big impact in image recognition. It became famous for its ability to classify images accurately. It won the ImageNet Large Scale Visual Recognition Challenge (ILSVRC) 2012 with a top-5 error rate of 15.3% (beating the runner up which had a top-5 error rate of 26.2%).

#### AlexNet Architecture

Its architecture includes:

- 5 convolutional layers with Max-Pooling applied after the 1st, 2nd and 5th layers to enhance feature extraction.

- Overlapping Max-Pooling uses a 3×3 filter with stride 2 which improved performance by reducing top-1 error by 0.4% and top-5 error by 0.3% compared to non-overlapping pooling.

- Followed by 2 fully connected layers each using dropout to prevent overfitting.

- Ends with a softmax layer for final classification.
- 
### VGG16

To improve performance, transfer learning was applied using the pretrained VGG16 model trained on ImageNet.

Two training phases were used:

- The convolutional base was frozen. Only the custom classification head was trained.

- The deeper convolutional layers were unfrozen. A smaller learning rate was used.

This allowed the model to adapt pretrained features to the target dataset.
VGG16-specific preprocessing was applied to match ImageNet training conditions.

### MobileNet

MobileNetV2, a lightweight architecture optimized for efficiency, was also evaluated using transfer learning.

Similar to VGG16, the model was trained in two stages:

- Frozen feature extraction
- Fine-tuning with a lower learning rate

MobileNetV2 uses depthwise separable convolutions, which significantly reduce the number of parameters compared to traditional CNN architectures.

## Methodology

1. Data preprocessing and cleaning

2. Train-validation-test data split

3. Image resizing and normalization

4. Data augmentation for improved generalization

5. Model training using TensorFlow/Keras

6. Model evaluation using accuracy and loss metrics

7. Testing on new unseen images

## Results

- VGG16 achieved the highest classification accuracy.

- Training and validation curves showed good convergence.

- The model was also tested on new images to evaluate real-world performance.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Google Colab

## Conclusion

This project demonstrates the effectiveness of deep learning techniques for driver behavior classification. The results show that CNN-based models can successfully identify distracted driving behaviors and have strong potential for real-world driver monitoring applications.

  
