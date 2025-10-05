# Summary week 4

Model Architecture Optimization for Small Dataset Classification

Image classification on the hymenoptera dataset (ants vs bees) presents a classic small-data challenge with only 120 training and 75 validation images per class. This limited data availability makes the model highly susceptible to overfitting, requiring careful hyperparameter selection.

Research Goal: Systematically investigate how different architectural choices affect model performance and generalization on small datasets, following proper scientific methodology.

Experimental Setup
    -Dataset: Hymenoptera (ants/bees) - 240 training, 150 validation samples
    -Base Architecture: Simple CNN with configurable layers
    -Fixed Parameters: Adam optimizer (lr=0.001), 15 epochs, batch size=32
    -Evaluation Metrics: Validation accuracy, overfitting gap, training stability


Here are the [instructions](./instructions.md) and here is a script to start [hypertune.py](./hypertune.py)

[Go back to Homepage](../README.md)
