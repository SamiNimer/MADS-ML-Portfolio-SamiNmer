# Summary week 2

Attempting Dropout and Normalization in CNNs

1. Hypothesis
I hypothesized that adding dropout and batch normalization to a convolutional neural network would improve generalization and reduce overfitting. Specifically:

Dropout would reduce co-adaptation of neurons and improve validation accuracy.

Batch normalization would stabilize training and accelerate convergence.

2. Experiment Design
I planned to:

-Modify the CNN architecture to include dropout after dense layers and batch normalization after convolutional layers.

-Use nn.ModuleList to flexibly stack convolutional blocks.

-Log hyperparameters and metrics using MLflow.

-Compare training and validation accuracy across different model variants.

3. Challenges Encountered
Despite having a clear plan, I encountered several issues:

-I added dropout to my model, but accidentally overwrote it with a different architecture (CNNblocks) that didn’t include dropout.

-I struggled to verify whether dropout was active during training.

-I wasn’t able to integrate MLflow logging successfully.

-I didn’t manage to run multiple experiments or visualize results due to time constraints and debugging difficulties.

4. Reflection
-Although I didn’t complete the experiments, I learned a lot about:

-How dropout and normalization layers are placed and used in PyTorch.

-The importance of managing model versions carefully.

-How frameworks like MLflow can support reproducibility and analysis.



Find the [instructions](./instructions.md)

[Go back to Homepage](../README.md
