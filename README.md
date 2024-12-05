# PRODIGY_ML_05
1. Data Preparation
For the initial 3 classes (apple_pie, pizza, omelette), images are prepared and their respective data folders are set up for training and validation.
A subset of 11 randomly chosen classes from the FOOD101 dataset is created for more complex training.
The dataset creation involves:
Copying relevant images into training and testing directories.
Ensuring equal distribution of samples across classes.
2. Data Augmentation
Applied using Keras' ImageDataGenerator with transformations such as rescaling, shearing, zooming, and horizontal flipping.
3. Model Architecture
ResNet50:
Pre-trained on ImageNet, with the top layers replaced.
Global average pooling followed by dense layers and dropout regularization.
Fine-tuned for:
3 classes initially.
Extended to 11 classes with categorical classification.
4. Training Process
Parameters:
Optimizer: Stochastic Gradient Descent (SGD) with momentum.
Loss: Categorical cross-entropy.
Regularization applied to the output layer.
Saved the best-performing model using ModelCheckpoint.
Training monitored with CSVLogger.
5. Performance Evaluation
Accuracy and loss plotted for both training and validation datasets.
Early stopping mechanisms ensured the model doesn't overfit.
6. Testing with New Images
Custom function predict_class:
Processes new images and predicts their classes.
Outputs predictions with visual plots.
7. Model Results
Initial training with 3 classes:
Demonstrated improvement in both accuracy and validation loss over epochs.
Fine-tuning on 11 classes:
Achieved over 92% validation accuracy by Epoch 26.
Incremental improvement in validation loss with best performance recorded.
