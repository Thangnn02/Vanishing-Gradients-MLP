# Vanishing Gradients MLP
Project revolves around addressing the vanishing gradient problem in MLP networks when training a deep model (with many hidden layers). There will be 6 different methods that impact the model training strategy, ... to help minimize vanishing gradients.
# Project Introduction
**Dataset:** FashionMNIST

**Methods:** In this project you will be introduced to 6 methods to reduce vanishing:
* **Weight Increasing:** The project requires you to initialize the weight with increased variance (or standard deviation) to minimize the vanishing problem in this project.
  - (a) mean = 0 and standard deviation = 1.0
  - (b) mean = 0 and standard deviation = 10.0
* **Better Activation:** The project requires you to change the activation function better to reduce the vanishing problem caused by the Sigmoid function. You will use the activation function ReLU after each hidden layer.
* **Better Optimizer:** The project requires you to change the optimizer algorithm better to reduce minimize the problem of disappearing. You will use the Adam algorithm for the optimizer and feed it to the compiler the model before training with a learning rate of 0.001.
* **Normalize Inside Network:** The project requires you to use the normalize technique internally network (specifically each hidden layer) to maintain the value of the transmitted information in a region with good derivatives. You will use the normalize layer in front of each hidden layer according to the following steps following requirements:
  - (a) Built-in BatchNormalization layer: torch.nn.BatchNorm1d()
  - (b) Custom normalize layer: $\frac{x-mean}{std}$
* **Skip Connection:** The project requires you to use the skip connection technique to the current model to minimize the vanishing problem.
  - **Step 1:** Make a skip connection path from the output of hidden layer 1 to the output of hidden layer 3.
  - **Step 2:** Make a skip connection path from the output of hidden layer 4 to the output of hidden layer 7.
* **Train Some Layers:** The project requires you to use the strategy of dividing the current model into 4 sub model and train 7 times with each time piling the sub models on top of each other and alternating freeze and unzfreeze weights of these sub models.
