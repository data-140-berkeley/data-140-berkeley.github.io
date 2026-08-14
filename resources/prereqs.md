---
layout: page
title: Math Prerequisites
nav_exclude: true
description: The prerequisites for the class.
---

{: .warning }
⚠️ The content on this site is archived and retained exclusively for reference. Updates will be made when the course is offered in the future.

# Math Prerequisities #
## A. Adhikari ##
{:.no_toc .text-delta}

## Table of Contents
{: .no_toc .text-delta }

- TOC
{:toc}

**The [course](/textbook) assumes [fluency](/resources/fluency) with all of the math below.** These concepts, results, and methods will be used without explanation. If you've forgotten some of it, please review the relevant materials. The more confident you are with this math content, the faster you will be able to grasp the material of the course.

**Please do the exercises.** They are based on calculations that come up frequently. 

Being able to **assess your own work** is an important mathematical skill and will be crucial in this course. If your answer to an exercise below doesn't match the one provided, or if you can't get started on an exercise,

- don't ask for a detailed solution.
- Remember that this is prereq material: you could do this stuff once upon a time. Maybe go back to your own previous class notes if you have them, or review the summaries here again, and examine your answer.
    - Which results did you use, and why?
    - Did you try a simpler version of the problem for which you can check your answer long-hand, for example by writing out all possibilities?
    - Did you draw a diagram?
    - Is your answer too big, or too small? Try to figure out which one, as it can help point out your error. If you can compare the question with another related one, that also can sometimes help explain the difference.
- After going through the above, try the exercise again a couple of times. 
- If it still doesn't work out, post on Ed explaining the reasoning that you used and which of the above steps you took to troubleshoot.

## Chapters 1-9, 12-14 ##

### Basic Counting ###

The number of finite sequences and subsets that can be created out of a finite set of objects:

**Review:** [Notation and Fundamental Properties](http://stat88.org/textbook/content/Chapter_03/00_Random_Counts.html). 

Notice the distinction between *sequences* (orderings, or "arrangements in a line") and *subsets* (unordered collections). You have to decide which is appropriate, by looking carefully at the context. In some probability calculations it won't matter which you decide to use, as long as you are consistent in the numerator and denominator of your proportions.

**Exercise BC1:** How many different ways are there to arrange six people 

**a)** in a row?

**b)** in a circle?


<details>
    <summary>
        Answer BC1
    </summary>
    <b>a)</b> 720 <br>
    <b>b)</b> 120 <br>
</details>  


**Exercise BC2:** A committee consists of six women and four men. How many different choices can be made if you want to select

**a)** a Chairperson and an Assistant Chairperson?

**b)** a subcommittee of two people?

**c)** a subcommittee of three men and three women?

<details>
    <summary>Answer BC2</summary>
    <b>a)</b> 90 <br>
    <b>b)</b> 45 <br>
    <b>c)</b> 80
</details> 

###  Sums ### 
Summation notation will be used throughout the term. For Chapters 1-7 you just need the following.

**Review:** [Terrific notes](http://www.cs.yale.edu/homes/aspnes/pinewiki/attachments/SummationNotation/summation-notation.pdf) by Prof. [James Aspnes](http://www.cs.yale.edu/homes/aspnes/) of Yale's CS department

"Sigma notation" is simply a compact way of making "..." precise when you are adding a bunch of terms. You've known the properties of sums since you started addition and multiplication in elementary school. The notation allows you to express those calculations concisely and precisely when the number of terms is large or when the terms being added are themselves functions.

- Review the definition in the first sentence of the notes. 
- Then go to Section 1.4 which has standard notation that we will use.
- You should understand (not just memorize) the first two sums in Section 2.1 on Page 5, and the first two identities in Section 2.2 on Page 6. There's a typo in the second one. It should read

$$
\sum_{i \in S} (x_i + y_i) ~ = ~ \sum_{i \in S} x_i + \sum_{i \in S} y_i.
$$

- Section 2.3 has excellent advice.
- In [Chapter 4](http://prob140.org/textbook/content/Chapter_04/01_Joint_Distributions.html) of the textbook you'll start working with double sums. The main idea is in Section 1.7 on Pages 4-5 of the Prof. Aspnes notes linked above; note the analogy with nested `for` loops. Useful properties are in the latter half of Section 2.2.

**Exercise S1:** Consider the sequence defined by $$c_i =i$$, for $$i=1, 2, \ldots , 10$$. If possible, find $$\sum_{k=1}^{10} c_k$$.  If this is not possible, explain why not.

<details>
    <summary>Answer S1</summary>
    55
</details> 

**Exercise S2:** Does the expression $$\sum_{n=1}^{10} 2$$ make sense?  If it does, what is its value?

<details>
    <summary>Answer S2</summary>
    20
</details> 

**Exercise S3:** Let $$\{c\}$$ and $$\{d\}$$ be sequences of real numbers so that 

$$
\sum_{i=1}^{100} c_i ~=~ 10 ~~~~\mbox{and} ~~~~~
\sum_{j=1}^{100} d_j ~=~ 20.
$$

**a)** Find the value of $$\displaystyle \sum_{i=1}^{100} (4c_i + 5)$$.

**b)** Find the value of $$\displaystyle \sum_{i=1}^{100} 4c_i ~+~ 5$$.

**c)** Find the value of $$\displaystyle \sum_{i=1}^{100} (4c_i - d_i + 5)$$.

**d)** True or false:

$$
\sum_{i=1}^{100} \sum_{j=1}^{100} (c_i + d_j) ~~=~~
\sum_{i=1}^{100} (c_i + d_i).
$$

If the identity is true, find the common value of the two sides. If it is false, find the values of the two sides.

<details>
    <summary>Answer S3</summary>
    <b>a)</b> 540 <br>
    <b>b)</b> 45 <br>
    <b>c)</b> 520 <br>
    <b>d)</b> False: \(\displaystyle \sum_{i=1}^{100} \sum_{j=1}^{100} (c_i + d_j)= 3000 \neq 30 = \sum_{i=1}^{100} (c_i + d_i)\)
</details> 

**Exercise S4:** Fill in the blanks:

$$
\sum_{i=1}^n \sum_{j=i}^n a_{ij}  ~ = ~ \sum_{j = \underline{~~~}}^{\underline{~~~}} \sum_{i = \underline{~~~}}^{\underline{~~~}} a_{ij}.
$$

[Hint: It might help to draw a grid of all $$(i,j)$$ pairs for some small value of $$n$$.]

<details>
    <summary>Answer S4</summary>
    \(\displaystyle \sum_{j = 1}^n \sum_{i = 1}^j a_{ij}\)
</details>

### Induction ###

Mathematical induction is a method that is sometimes helpful for proving math statements if:

- You have a guessed a math statement for each positive integer $$n$$, where the $$n$$th statement depends on $$n$$, and
- for small $$n$$ (even just $$n=1$$) you can easily show that the statement is true.

**Review:** A [clear set of notes](http://www.math.utah.edu/mathcircle/notes/induction.pdf) from [Tom Davis](https://mathcircle.berkeley.edu/tom-davis) of the Berkeley Math Circle 

- Just go through Pages 1 and 2

The method is always the same.

- Prove the base case.
- Assume the induction hypothesis. That is, assume that the statement is true for a generic integer $$n$$.
- Write the statement for $$n+1$$. This is what you have to prove.
- [This is where the bulk of the work comes in.] Somehow write the statement for $$n+1$$ in terms of the statement for $$n$$ (assumed to be true) and the base case (which you have proved), in such a way that a little algebraic or other mathematical messing around show that the statement for $$n+1$$ is true.

**Exercise I1:** Show by induction that for each positive integer $$n$$, 

$$
\sum_{i=1}^n i ~ = ~ \frac{n(n+1)}{2}.
$$

<details>
    <summary>Answer I1</summary>
    The key step is \(\displaystyle \sum_{i=1}^{n+1} i = \sum_{i=1}^n i + (n+1)\).
</details> 

**Exercise I2:** Apply I1 (no induction necessary) to find 

$$
\sum_{i=0}^{n-1} i.
$$ 

This is the form in which the result first appears in the course, in [Chapter 1](http://prob140.org/textbook/content/Chapter_01/05_An_Exponential_Approximation.html) of the textbook.

**Exercise I3:** Use I1 and properties of sums (no induction necessary) to find a simple expression for the sum of the first $$n$$ ***odd*** integers:

$$
\sum_{i=1}^n (2i-1).
$$

**Exercise I4:** As a check, use induction to prove the formula you got in I3.

### The Exponential and Log Functions ###

**NOTE: All $$\log$$s in this class, and in almost all of math, are natural logarithms taken to the base $$e$$.**

You know that $$\log(1) = 0$$. What we're going to need, quite often, is an approximation for the log of a number that is very close to 1. A crude approximation is 0 because the number is close to 1. But we'll use a finer approximation based on the first couple of terms in a related Taylor expansion.

**Review:** [Graphs and Relevant Properties](http://prob140.org/resources/exponential_approximations/). For now, you need the *Limits and Approximations* section but not the *Bounds*. Preferably, you should understand the approximations in relation to the graphs of $$e^x$$ and $$\log(x)$$.

- In [Chapter 1](http://prob140.org/textbook/content/Chapter_01/05_An_Exponential_Approximation.html) you'll need the approximations.
- Starting with [Chapter 6](http://prob140.org/textbook/content/Chapter_06/06_Law_of_Small_Numbers.html#poisson-approximation-to-the-binomial) you'll need the Taylor expansion of $$e^x$$.

**Exercise EL1:** About how big is 

**a)** $$\log(1.01)$$?

**b)** $$\log(0.99)$$?

<details>
    <summary>Answer EL1</summary>
    <b>a)</b> \(0.01\) <br>
    <b>b)</b> \(-0.01\)
</details>  


**Exercise EL2:** Suppose $$0 < p_n < 1$$ for all $$n$$, $$\lim_{n \to \infty} p_n = 0$$, and $$\lim_{n \to \infty} np_n = \mu$$ for some number $$\mu > 0$$. Find  $$\lim_{n \to \infty} (1 - p_n)^n$$. 

[Hint: Start by considering the $$\log$$ of $$(1 - p_n)^n$$. Approximate it for large $$n$$, and then invert.]

<details>
    <summary>Answer EL2</summary>
    \(e^{-\mu}\)
</details>  

**Exercise EL3:** In EL2, $$1 - p_n \to 1$$ as $$n \to \infty$$, and $$1^n = 1$$ for all $$n$$. So why isn't it true that $$(1 - p_n)^n \to 1$$ as $$n \to \infty$$?

<details>
    <summary>Answer EL3</summary>
    \(\text{For a fixed power }m\text{, it's true that }(1 - p_n)^m \to 1\text{ as }n \to \infty\text{.}\)<br>
    \(\text{ But in the expression }(1 - p_n)^n\text{ the power }n\text{ isn't fixed. It's going to infinity.}\)<br>
    \(\text{So the sequence }(1-p_n)^n\text{ is pulled in opposite directions: }1-p_n\text{ is heading for its}\)<br>
    \(\text{ upper limit of 1, but it's always less than 1 and so raising it to an increasing power }n\text{ keeps pulling it downwards.}\)
</details> 

**Exercise EL4:** Computers can't do infinite sums (though they can get close numerically, and some symbolic math systems can handle many infinite sums). Find simple expressions for the following sums.

**a)** $$\displaystyle \sum_{n=0}^{\infty} \frac{1}{n!}$$

**b)** $$\displaystyle \sum_{i=0}^{\infty} \frac{2^{3i}}{i!}$$

**c)** $$\displaystyle \sum_{k=2}^{\infty} \frac{3^k}{k!}$$

**d)** $$\displaystyle \sum_{i=0}^\infty \frac{2^i}{(i+1)!}$$

<details>
    <summary>Answer EL4</summary>
    <b>a)</b> \(e\) <br>
    <b>b)</b> \(e^8\) <br> 
    <b>c)</b> \(e^3 - 4\) <br>
    <b>d)</b> \(\frac{1}{2}(e^2 - 1)\)
</details>  

### Geometric Series ###

We'll use the infinite series more frequently than the finite one, starting in [Chapter 8](http://prob140.org/textbook/content/Chapter_08/02_Applying_the_Definition.html#geometric) of the textbook. In fact the infinite series is easier to sum (provided you assume it's finite, which it's fine for you to do), and then you can derive the finite series sum from the infinite one, as in the notes linked below.

**Review:** The main results on Page 6 (Section 2.1) of [Prof. Aspnes notes](http://www.cs.yale.edu/homes/aspnes/pinewiki/attachments/SummationNotation/summation-notation.pdf). Understand the derivation of the infinite sum. That way you'll never have to memorize the results.

**Exercise GS1:** Let $$0 < p < 1$$. Let $$\displaystyle S = \sum_{i=0}^{\infty} p^i$$.

**a)** Find $$S$$.

**b)** Replace the $$?$$ with the appropriate factor: $$\displaystyle \sum_{i=3}^{\infty} p^i  = ? \cdot S$$. Hence find $$\displaystyle \sum_{i=3}^{\infty} p^i$$.

**c)** Find $$\displaystyle \sum_{i=0}^{\infty} p^{3i}$$.

<details>
    <summary>Answer GS1</summary>
    <b>a)</b> \(\dfrac{1}{1-p}\) <br>
    <b>b)</b> The factor is \(p^3\) so the sum is \(\dfrac{p^3}{1-p}\) <br>
    <b>c)</b> \(\dfrac{1}{1-p^3}\)
</details>  

## Chapters 10-11 ##

### Basic Matrix Operations ###

That's all we'll need for these two chapters. Linear algebra will be used more significantly towards the end of the course.

By the time you get to Chapter 10 you will have realized that probability is all about weighted averages. Matrix representation gives us a compact and powerful way to work with these. For example, suppose $$\mathbf{x} = x_1, x_2, \ldots, x_n$$ is a list of numbers and $$\mathbf{w} = w_1, w_2, \ldots, w_n$$ is a list of weights that add up to $$1$$. Then the dot product $$\mathbf{w\cdot x}$$ is the weighted average of $$\mathbf{x}$$ using $$\mathbf{w}$$ as the weights. 

**Review:** It is important to visualize the sizes and shapes of the vectors and matrices involved. Prof. [Semyon Dyatlov](http://math.mit.edu/~dyatlov/) of MIT has a [nice summary](http://math.mit.edu/~dyatlov/54summer10/matalg.pdf) of the basic matrix operations, which I believe was written when he taught Math 54 as a graduate student at Berkeley. Notice that he starts with just the sizes, before going into the algebra.

**Exercise MO1:** Let $$\mathbf{A}$$ be $$n \times m$$ and let $$\mathbf{v}$$ be a vector.

Fill in the first blank with either *row* or *column*, and the second with either $$n$$ or $$m$$.

For $$\mathbf{vA}$$ to make sense, $$\mathbf{v}$$ must be a ______ vector of length ______.

<details>
    <summary>Answer MO1</summary>
    row, \(n\)
</details>  

In the following exercises, assume the conditions of MO1 and that $$\mathbf{vA}$$ makes sense.

**Exercise MO2:** Fill in the first blank with either *row* or *column*, and the second with either $$n$$ or $$m$$.

$$\mathbf{vA}$$ is a ______ vector of length ______.

<details>
    <summary>Answer MO2</summary>
    row, \(m\)
</details>  

**Notation** for MO3-MO5: Let $$\mathbf{A}(i, j)$$ be the $$(i, j)$$ element of $$\mathbf{A}$$, $$\mathbf{A}(i, *)$$ the $$i$$th row of $$\mathbf{A}$$, and $$\mathbf{A}(*, j)$$ the $$j$$th column of $$\mathbf{A}$$. Let $$\mathbf{v}(j)$$ be the $$j$$th element of $$\mathbf{v}$$.

**Exercise MO3:** Write the $$j$$th element of $$\mathbf{vA}$$ using sigma notation.

<details>
    <summary>Answer MO3</summary>
    \(\displaystyle \sum_{i=1}^n \mathbf{v}(i)\mathbf{A}(i, j)\)
</details>

**Exercise MO4:** True or false: The elements of $$\mathbf{vA}$$ are $$\mathbf{v}\cdot\mathbf{A}(*, 1), \mathbf{v}\cdot\mathbf{A}(*, 2), \ldots, \mathbf{v}\cdot\mathbf{A}(*, m)$$.

<details>
    <summary>Answer MO4</summary>
    True
</details>

**Exercise MO5:** Now suppose $$\mathbf{A}$$ is $$n \times n$$ for $$n \ge 5$$. Fill in the first blank with the right coordinates and the second with a matrix:

$$\sum_{k = 1}^n \mathbf{A}(2, k)\mathbf{A}(k, 5)$$ is the ______ element of the matrix ______.

<details>
    <summary>Answer MO5</summary>
    \((2, 5)\), \(\mathbf{A}^2\)
</details>

## Chapter 15 onwards ##

### Calculus ###

Here are two excellent resources for refreshing your memory.
- Prof. Paulin's [Math 1A](https://math.berkeley.edu/~apaulin/Teaching.html) lectures; click on Complete Course Video Lectures
- An excellent [single variable calculus](https://ocw.mit.edu/courses/18-01-single-variable-calculus-fall-2006/pages/lecture-notes/) course from MIT

Topics worth remembering:
- The [Fundamental Theorem](https://ocw.mit.edu/courses/18-01-single-variable-calculus-fall-2006/resources/lec20/) of calculus, from the MIT course above
- The [derivative of an inverse function](https://ocw.mit.edu/courses/18-01-single-variable-calculus-fall-2006/resources/lec5/), from the same MIT course; a simple result that has a useful application in probability
- A discussion of the [absolute convergence of integrals](https://web.math.princeton.edu/~nelson/104/ImproperIntegrals.pdf) from [Prof. Edward Nelson](https://web.math.princeton.edu/~nelson/) of Princeton
- A [double integral](https://www.youtube.com/watch?v=YP_B0AapU0c) lecture video by [Denis Auroux](http://people.math.harvard.edu/~auroux/); examples are at 19:40 and 28:15

## Chapter 23 onwards ##

### More Linear Algebra ###

Recall the Basic Matrix Operations, above. You will also need the following summaries of properties.

- [Positive definite matrices](http://wwwf.imperial.ac.uk/~das01/MyWeb/M3S3/Handouts/Positive.pdf) by [Prof. David Stephens](http://wwwf.imperial.ac.uk/~das01/MyWeb/index.html) written when he was at Imperial College
- [Dot Products](http://sites.math.washington.edu/~king/coursedir/m445w04/notes/vector/dotproduct.html) by [Prof. James King](https://math.washington.edu/people/james-r-king) of U. Washington at Seattle.
