# GhostMixNet
## Abstract
In this work, we analyze the effectiveness of various pre-processing and attention mechanisms, as well as GhostNet modules, in the training and validation of a ResNet architecture with only 3 million parameters. Trained and evaluated on the CIFAR-10 dataset, the model reaches 95.5\% accuracy on the validation data, despite the operations being cheap enough to run on mobile or IoT devices.
## Training Setup:
### Optimizer: 
AdamW with Beta1 of 0.9 Beta2 of 0.999 and weight decay of 0.001.
### Data Augmentation: 
RandomCrop, RandomHorizontalFlip, RandomPerspective, RandomPosterize, ColorJitter, AutoAugment, Mixup and CutMix.
### Regularization:
Dropout with a probability of 0.2 was used to combat overfitting.
### Learning Rate and Schedule:
Started with a Learning Rate of 0.001 and used a Cosine Annealing Warm Restarts scheduler, with warm restarts after 50 epochs.
### Batch Size and Epochs:
A batch size of 128 and trained for up to 200 epochs.
