# Summary week 1
Lorem ipsum dolor sit amet, consectetur adipiscing elit.

Find the [notebook](./notebook.ipynb) and the [instructions](./instructions.md)

## First Run

At first, I ran the experiment without making any changes, just to get a sense of how everything works. Before executing the code, I took time to read through it carefully and tried to understand its structure and logic.

While reading, I encountered a question embedded in the code: "Why do you think I call it naive?" I believe the model is described as naive because it's relatively simple and hasn't been trained extensively. It uses a basic architecture and runs for only 3 epochs with 100 training steps. In my view, it's still in the early stages of learning—almost like it's guessing. That forms the basis of my null hypothesis: the model is naive due to its simplicity and limited training.

After visualizing the model, I’ll evaluate whether the evidence supports or refutes that hypothesis.

Looking at the test loss, we observe a clear downward trend, which suggests the model is improving over time and learning from the data.

<img width="1726" height="544" alt="image" src="https://github.com/user-attachments/assets/95c04cf8-9f11-4c9c-b422-edb7112f462d" />

but the loss is still high

Wall time----Step---Value

1757440345---0------0.666404963

1757440346---1------0.558107376

1757440347---2------0.51867193

We observe the same downward trend with the trening loss

<img width="1725" height="531" alt="image" src="https://github.com/user-attachments/assets/6dcb7c1b-6b65-40c1-bed3-121b09ec9fe3" />

## Second Run

Null Hypothesis: Improved Performance

In the second run, I introduced three additional linear layers, each followed by a non-linear activation function, resulting in a total of five layers. The first two layers were configured using a loop, while the remaining three hidden layers were manually set to 64, 32, and 16 units respectively. I also increased the number of training epochs from 5 to 10, keeping the number of learning steps fixed at 100.

These modifications led to a noticeable improvement in the neural network’s performance. Based on the results, I failed to reject the null hypothesis that the model would perform better with a deeper architecture and extended training.

<img width="2135" height="1032" alt="image" src="https://github.com/user-attachments/assets/ada2647f-bd31-410c-8dd0-5745bc1969a8" />

## Third Run

Null Hypothesis: Improved Performance

For the third run, I maintained the same five-layer architecture, with each layer followed by a non-linear activation function. This time, I set the number of hidden units in each layer to 100 and trained the model for 20 epochs. As expected, increasing both the depth of the network and the number of training epochs resulted in a noticeably longer training time.

While the model's performance did improve compared to the second run, the gains were modest. Given the extended training duration, I had anticipated a more substantial improvement. Therefore, although the null hypothesis of improved performance holds, the results were less impressive than expected.

<img width="2149" height="1118" alt="image" src="https://github.com/user-attachments/assets/7e77cbbc-5d10-4d89-b9da-ff24394e30b4" />

## Fourth Run

Null Hypothesis: More Is Better

In the fourth run, I expanded the architecture to include 10 layers, each containing 200 hidden units. The model was trained for 20 epochs, with 100 learning steps per layer. Despite the increased depth and capacity, the performance declined—clearly illustrated by the red line in the screenshot below.

Conclusion: More is not always better. Increasing the number of layers and units did not lead to improved results and instead negatively impacted performance.

<img width="2157" height="1112" alt="image" src="https://github.com/user-attachments/assets/e4033d10-0cc4-4187-9770-76740a68db76" />


One advantage of increasing the number of epochs is that it gives the model more time to learn and refine its predictions. However, this comes with trade-offs: longer training time and a potentially higher risk of overfitting. If the model continues to improve and the loss keeps decreasing, extending the number of epochs can be beneficial—up to a certain point. Beyond that, the gains may diminish or even reverse.

[Go back to Homepage](../README.md)
