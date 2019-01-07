---
layout: post
title: ML
category: Machine-Learning
tags: [Machine-Learning]
---

# Overview of Supervised Learning
teminology:(the former often used in statistical literature and the latter often used in machine learning)
+ predictors(features): inputs
+ responses(dependent variable): outputs

conventitions:
1. \(X\)- denote an input variable
2. $X_{j}$- denote the jth component of vector $X$
3. $Y$- denote quantitative outputs
4. $G$- qualitative outputs
5. Obversed values are written in lowercase, hence the $i$th observed value of $X$ is written as $x_{i}$
6. Matrices are represented by bold upcase letters


After introducing conventions above, we state the learning task as follows:
given the value of an input vector $X$, make a good prediction of the output $Y$, denoted by $\hat{Y}$. If $Y$ takes values in $R$ then so should $\hat{Y}$ ; likewise for categorical outputs, $\hat{G}$ should take values in the same set $g$ associated with $G$.


Next, we need data to construct prediction rules, that is,
we have available a set of measurements $(x_{i}, y_{i})$ or $(x_{i}, g_{i})$, $i = 1, \ldots, N$, known as the training data
