# Summary week 3

My Learning Journey: Building Better Neural Networks for Gesture Recognition
What I Learned About the Data
I started by understanding the gesture data we're working with. Each gesture is a sequence of movements, like someone drawing shapes in the air. The data comes as:

•	32 sequences at a time (called "batches")

•	27 time steps in each sequence (though this can change)

•	3 measurements at each step (probably x, y, z coordinates from a sensor)

I learned that sequences can have different lengths, so we use "padding" to make them the same size for processing. This was a new concept for me.
Setting Up My Experiments
I got TensorBoard and MLflow working to track my experiments. At first, TensorBoard was empty and I had to figure out why. This taught me how to:

•	Check if log files are being created

•	Fix missing parameters (like the scheduler)

•	Start TensorBoard properly

Seeing 7 different experiment files in TensorBoard and 10 runs in MLflow showed me that everything was working. It felt good to solve these technical problems.
Understanding How the Model Works
I built a GRU model (a type of neural network good for sequences) and learned:

•	How it processes sequences step by step

•	Why we use the last step for classification

•	What all those numbers in the output mean

•	How the model learns from its mistakes using loss calculation

The most helpful part was seeing how the data flows through the model - from 32 sequences with 27 steps each, down to 32 predictions about what gesture was made.

My Approach to Improvement

Instead of trying fancy changes right away, I learned to:

1.	Start simple - get a basic model working first

2.	Change one thing at a time - so I know what actually helps

3.	Track everything - using TensorBoard and MLflow

4.	Learn from mistakes - like when I forgot the scheduler

This methodical approach helped me understand what I was doing instead of just copying code.
Challenges I Faced and Overcame

•	TensorBoard not showing anything - I learned to check the log files and fix the directory structure

•	Missing scheduler error - I figured out what was missing and fixed it

•	Understanding the data shapes - It took time to understand what (32, 27, 3) really means

Each problem I solved made me more confident about working with neural networks.

What I Can Do Now

I feel comfortable with:

•	Building simple neural networks in PyTorch

•	Setting up experiment tracking

•	Understanding how sequence data works

•	Debugging when things go wrong

•	Making small improvements to models

Most importantly, I learned how to approach problems step by step, which will help me with future projects.

Ready for the Next Steps

I'm now prepared to try different model architectures and work toward that 90% accuracy goal. I understand the foundation, so I can experiment intelligently rather than randomly trying things.

The biggest lesson was that starting simple and building up gradually is much better than trying to understand everything at once. I'm excited to continue improving my model and seeing how high I can get the accuracy!



Lorem ipsum dolor sit amet, consectetur adipiscing elit.

Find the [notebook](./notebook.ipynb) and the [instructions](./instructions.md)

[Go back to Homepage](../README.md)
