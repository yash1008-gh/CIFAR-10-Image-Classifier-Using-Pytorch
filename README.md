# CIFAR-10 Image Classification using PyTorch

This is my first CNN project built while learning PyTorch. The goal of this project was to understand the complete deep learning workflow, from loading data to training, saving, and testing a neural network.

The model is trained on the **CIFAR-10** dataset, which contains 60,000 color images belonging to 10 different classes.

## Classes

* plane
* car
* bird
* cat
* deer
* dog
* frog
* horse
* ship
* truck

## What I Learned

* Loading datasets using `torchvision`
* Image preprocessing and normalization
* Building a CNN using `nn.Module`
* Forward propagation
* Loss calculation using `CrossEntropyLoss`
* Backpropagation and weight updates
* Saving and loading model weights
* Evaluating model performance

## Model Architecture

```text
Input (3 × 32 × 32)

→ Conv2d(3, 6, kernel_size=5)
→ ReLU
→ MaxPool2d(2 × 2)

→ Conv2d(6, 16, kernel_size=5)
→ ReLU
→ MaxPool2d(2 × 2)

→ Flatten

→ Linear(16 × 5 × 5, 120)
→ ReLU

→ Linear(120, 84)
→ ReLU

→ Linear(84, 10)
```

## Training Details

* Optimizer: SGD with Momentum
* Learning Rate: 0.005
* Loss Function: CrossEntropyLoss
* Epochs: 5
* Batch Size: 5

## Results

Class-wise accuracy obtained after training:

| Class | Accuracy |
| ----- | -------- |
| Plane | 24.3%    |
| Car   | 75.8%    |
| Bird  | 27.7%    |
| Cat   | 50.9%    |
| Deer  | 35.0%    |
| Dog   | 32.5%    |
| Frog  | 49.5%    |
| Horse | 60.8%    |
| Ship  | 68.5%    |
| Truck | 36.3%    |

The model performs reasonably well on some classes such as **car**, **ship**, and **horse**, but struggles with classes that have similar visual features. Since this was built mainly for learning PyTorch basics, the focus was understanding the training pipeline rather than achieving high accuracy.