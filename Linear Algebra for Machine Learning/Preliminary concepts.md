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
Τhe colon （:） or vertical bar （|）read as "such that".

## Ordered pairs
**An unordered pair** is a set whose elements are $x,y$, and $x,y=y,x$. Therefore, presentation order does not matter, the set is the same.

In machine learning, we usually **do** care about the presentation order. So we need to define an ordered pair.
An **ordered pair** is denoted as $ \left(x,y\right) $, with $x$ as the *the first coordinate* and $y$ as the *second coordinate*. $ \left(x,y\right)\neq\left(y,x\right)$.

## Relations
We can derive the idea of **relations** among sets or between elements and sets