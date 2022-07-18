# NeuralNetworks_OptionPricing

In this project we aim to build an ANN from scratch to value financial options with the four following purposes: firstly, obtaining the possible exactness of our predictions, so there is no difference with the use of the parametric option pricing model; secondly, accelerating these corresponding models, since the real-world problems of this field make the use of these models unfeasible, due to the requirement of massive computations in a daily basis; thirdly, estimating the Greeks associated to our financial option using a Gradient Tape technique with our trained ANN, in order to see if it is possible to compute them using our approach accurately, and not one where the ANN directly outputs these Greeks; and lastly, we aim to build a hyper- parameter optimization algorithm that could potentially be extended to any pricing model, with close and non-close formula. Additionally, we evaluate its computational cost and briefly comment on its real-life scalability.

The structure of this repository is the following:

\begin{enumerate}
    \item \textbf{data}: folder containing the simulated data.
    \begin{itemize}
        \item \textit{data\_lists}: first simulation.
        \item \textit{final\_data}: Greeks added.
    \end{itemize}
    \item \textbf{final\_neural\_network}: folder containing the final neural networks, fully trained and optimized, for the Original and Greeks models.
    \item \textbf{final\_results}: folder containing results organized accordingly to the training phase they belong to. In each of the following sub-folders, there are 4 files: the saved model, its weights, the optimized parameters and the history results, which contain the loss (MSE) and metric ($R^2$) for the training and validation data at each epoch.
    \begin{itemize}
        \item \textit{200\_epochs\_results}: last fit of the optimized model, increasing the number of epochs from 50 to 200 (using a patience of 10).
        \item \textit{200\_epochs\_results\_greeks}: last fit of the optimized model used to compute the Greeks, increasing the number of epochs from 50 to 200 (using a patience of 10).
        \item \textit{grid\_results}: results obtained with a GridSearch of 4 fits (batch normalization and dropout) and cross-validation of 10.
        \item \textit{grid\_results\_greeks}: results obtained with a GridSearch of 4 fits (batch normalization and dropout) and cross-validation of 10, for the Greeks model.
        \item \textit{randomsearch\_results}: first results obtained through the RandomSearch, with 100 fits and cross-validation of 3.
        \item \textit{randomsearch\_results\_greeks}: first results obtained through the RandomSearch, with 100 fits and cross-validation of 3, for the Greeks model.
    \end{itemize}
    \item \textbf{images}: folder containing the final model schemes (vertical and horizontal), for both Original and Greeks models.
    \item \textbf{results\_search}: folder where results were saved when running the training phases. They are all mixed, so go to \textbf{final\_results} for better understanding.
    \item \textbf{simulation}: folder containing the notebooks regarding the simulation of financial data.
    \begin{itemize}
        \item \textit{DATA\_1\_simulation}: first simulation.
        \item \textit{DATA\_2\_final}: Greeks added.
    \end{itemize}
    \item \textbf{training\_NN}: folder contianing the notebooks where the networks were trained. Ordered per training phase: 1 for RandomSearch, 2 for GridSearch and 3 for the last fit with 200 epochs.
\end{enumerate}
