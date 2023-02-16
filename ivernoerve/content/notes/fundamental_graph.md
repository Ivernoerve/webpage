---
title: "Fundamental graph theory"
date: 2022-12-27T10:55:17+01:00
draft: false
math: true
categories: 
 - math
---


A graph is a set of vertices (nodes) and a set of edges (links) connecting the graphs together creating a dataset with relational information. Formally a graph $G$ is defined as an ordered pair of a set of vertices $V$ and a set of edges $E$; $G =(V,E)$ 

Further the edges can have more properties such as directionality: A directional graph will have edges that can be traversed in certain directions; given two vertices $A,B$ and a edge between tham $AB$, if the graph is directed, the traversal can only happen from $A$ to $B$ since the edge connecting them only has a link in the $AB$ direction and not the $BA$ direction. Indicating that for a directed graph, two edges must go between a pair of vertices to allow for traversal both ways. 

Another property a graph can have is weighted edges auch that each edge has a numerical weight assigned to them corresponding to a feature we want to model. Examples of a weighted graph could be the global transport system where we want to find the best compromise betweeen transport times and cost, in such a case each vertice can represent a shipping station, and the edges can have two weights assigned to them; one for cost and one for time. 


A lot of problems, and scenarioes can ba modeled by a graph, a shipping problem was mentioned above, but it can also be used to understand statistical models such as a discrete time markov chain (weighted directed graoh where the weights indicate the transition probabilities.) as well as fundamental data structures used in computer scinence (linked lists, and binary trees can both be understood as a directional graph).