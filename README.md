# Small-n-Accurate-CIFAR10-model
model with ONLY 620K parameters reaching 85% validation accuracy in CIFAR10 dataset

# Efficiency Analysis
- ~85% accuracy with only <1% of VGG-16's parameters and <6% of ResNet-18's parameters
- Great generalization. Only 0.6% difference between train/test accuracy (85.1% vs 84.5%).

# Primary Optimization
- dropout in fully connected layers
- vgg style consecutive convolution in early layers
- Data augmentation (flipping, random cropping, color jittering, standard normalization)

# Secondary optimization (things that didn't contribute a lot)
- Resnet-style "BatchNorm layers before activation"
- small dropouts after pooling
- early exit from training based on validation loss
