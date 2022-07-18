# NeuralNetworks_OptionPricing

In this project we aim to build an ANN from scratch to value financial options with the four following purposes: firstly, obtaining the possible exactness of our predictions, so there is no difference with the use of the parametric option pricing model; secondly, accelerating these corresponding models, since the real-world problems of this field make the use of these models unfeasible, due to the requirement of massive computations in a daily basis; thirdly, estimating the Greeks associated to our financial option using a Gradient Tape technique with our trained ANN, in order to see if it is possible to compute them using our approach accurately, and not one where the ANN directly outputs these Greeks; and lastly, we aim to build a hyper- parameter optimization algorithm that could potentially be extended to any pricing model, with close and non-close formula. Additionally, we evaluate its computational cost and briefly comment on its real-life scalability.

The structure of this repository is the following:


