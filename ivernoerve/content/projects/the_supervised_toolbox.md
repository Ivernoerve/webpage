---
title: "The Supervised Toolbox"
date: 2023-09-26T10:43:14+02:00
draft: true
imgpath: nn.png
git:
math: true
---

This project aims to uncover some properties in different supervised classification algorithms. Is there a **one to rule them all** algorithm? Let us delve in!

We will be looking at three different model arhcitectures, narely Neural networks, trees or ensembles of trees, and a K nearest neighbour model. 


All of these models are capable of creating non linear decision boundaries, however the underlying assumptions are quite different resulting in potentially differnt boundaries. 

## Some explanations 
All the plots shown below displays the data in a scatterplot colored by class. The background shows the classification boundary for the given classifier. The color corresponds to the colors of the classes in the data. The boundary the gradients in the background shows the certainty of the classification, i.e a more intense color indicates higher certainty.


## Results

### Neural network
For this classification task a simple 1 hidden layer neural network (*NN*) was created, each linear layer is followed by a relu activation with a sigmoid function applied to the output. 

As expected the *NN*'s decisiondecision boundary is highly nonlinear with smoothly varying certainties towards the regions where class boundaries meet.

{{< project-image "nn.png" >}}
### decision tree 

The decision tree is a traditional machine learning algorithm that makes classifications by learning a set of splits across the features which allows for a non linear decision boundary. The figure below shows a boundary created by a decision tree with no limit on the depth it is allowed to train for. As described it can be observed that each area is separated by linear cuts along the two features.

{{< project-image "tree.png" >}}

### Random forest

The random forest can be thought of as an extention to the decision tree. It is an ensemble algorighm meaning that it contains many classifiers that all contributes to the total classification. A decision tree is a deterministic algorithm, meaning that given the same dataset a decision tree will always converge to the same solution. Thus to be able to train several trees the dataset is bootstrapped to simulate several synthetic datasets to use for training the ensemble. 

Observing the figure below it can be observed that the decision boundary depends on the number of trees in the ensemble. An advantage to the random forest is the robustness in the certainty given for a classification. Notice how the red class has a high certainty closer to the cluster than for the single decision tree.

{{< project-image "forest.png" >}}

### K nearest neighbour

The K nearest neighbour classifier classifies is another traditional algorithm that classifies a sample directly by looking at the closeness to an underlying distribution estimated from some training data. The choice of K is important to get a robust enough classifier. Observe for the K-nn with K=1, that the extrema points of each class creates small islands in the classification boundaries that allows for bad generalization. When increasing the K such as for the K = 5, the generalization problem is mitigated.

{{< project-image "knn.png" >}}



## Is there a clear winner?

Observing the different decission boundaries, it is clear that the different algorithms results in widely differnt boundaries. Naturally the tree classifiers has shared trends in its boundaries as they are based on tree. The Neural Network creates a higly nuanced boundary with varying certainty, however it is the algorithm that is hardest to interpret in terms of why the classifications turn out the way the do. The Knn classifier gives a boundary similar to the neural network, however the certainty regions are less nuanced than the neural network. 

From the small paragraph above it is clear that all the mentioned algorihms has advantages and drawbacks to them. They all can 