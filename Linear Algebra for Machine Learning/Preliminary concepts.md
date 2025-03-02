# Preliminary concepts
## Sets
Sets are well-defined collections of objects. Such Objects are called **elements if members** of the set. *Vectors* are sets of points, and *matrices* are sets of vectors.

---

## Belonging and inclusion
Βelonging:  $$
a\in A
$$

A is a *subset* of B, or B includes A:$$ 
A \subset B
$$

Two sets are equal if and only if they have the *same elements*.

## Set specification
D: the set of all dogs
d: dog
*The set of all black dogs*: 
$$
B= \left\{d\in D: d\ is\  black\right\}
$$
οr
$$
B= \left\{d\in D|\, d\ is\ black \right\}
$$
Τhe colon $\left(\ :\ \right)$ or vertical bar $\left(\ :\ \right)$ read as "such that".

## Ordered pairs
**An unordered pair** is a set whose elements are $x,y$, and $x,y=y,x$. Therefore, presentation order does not matter, the set is the same.

In machine learning, we usually **do** care about the presentation order. So we need to define an ordered pair.
An **ordered pair** is denoted as $ \left(x,y\right) $, with $x$ as the *the first coordinate* and $y$ as the *second coordinate*. $ \left(x,y\right)\neq\left(y,x\right)$.

## Relations
We can derive the idea of **relations** among sets or between elements and sets. In set theory, **relations** are defined as *sets of ordered pairs*, and denoted as $R$. We can express the relation between $x$ and $y$ as:
$$
x\ R\ y
$$
Further, for any $z \in R$, we can obtain the notions of **domain** and **range**. The domian is a set defined as:
$$
dom R = \left\{x:\ for\ some\ y\ \left(x\ R\ y\right)\right\}
$$
This reads as: the values of $x$ such that for at leat one element of $y$, $x$ has a relation with $y$. The **range** is a set defined as:
$$
ran R = \left\{y:\ for\ some\ x\ \left(x\ R\ y\right)\right\}
$$
This reads as: the set formed by the values of $y$ such that at least one element of $x$, $x$ has a relation with $y$.

## Fuctions
A **function** from $X$ to $Y$ is a relation such that:
>>$dom f = X$
>>such that for each $x \in X$ there is a unique element of $y \in Y$ with $\left(x,y\right) \in f$

We can say that a function "transform" or "map" or "sent" $x$ onto $y$, and for each "argument" $x$ there is a unique value $y$ that $f$ "assumes" or "takes".

We typically denote a relation a relation or function or transformation or mapping from $X$ onto $Y$ as:
$$
f: X\ \rightarrow\  Y
$$
or
$$
f(x)\ =\ y
$$

Each value $f\left(x\right)$ maps uniquely onto one value of $y$.
For $f: X\ \rightarrow\  Y$, the domain of $f$ equals to $X$, but the range does not necessarily equals to $Y$. The range includes only the elements for which $Y$ has a relation with $X$.

**The ultimate goal of machien learning is learning functions from data.**
The domain $X$ is usually a vector (or set) of *variables* or *features* mapping onto a vector of *target values*. 