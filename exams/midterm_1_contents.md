---
layout: page
title: Midterm 1 Contents
nav_exclude: false
description: Scope for Midterm 1.
---

### Data 140 Fall 2026 ###
### A. Adhikari ###

# Material for Midterm 1 #
<br>
Midterm 1 is on Monday 9/28 from 8:10 PM to 9:40 PM. The scope is Chapters 1 through 9. 

Here is a summary of the material for the exam, grouped by main topic. **Boldface** has been reserved for topics that we consider to be **core material** for understanding the rest of the course.

The general techniques are in the sections Probability, Distribution, and Expectation. The Random Counts section consists of applications. 

In several chapters, **the book has sections called Examples. Please review those.** Please also review all your homework, labs (the mathematical parts; see the list at the end of this doc), and exercises done in section.

You will not have to write code on the midterm. Any code that you may have to read will be straightforward with comments that explain exactly what it is doing.

---

### Probability ###
- [Chapter 1](https://data140.org/textbook/content/chapter-01/fundamentals/), Lab 1: Spaces, events, basic counting, exponential approximation
- **[Chapter 2](https://data140.org/textbook/content/chapter-02/calculating-chances/)**, [Section 9.1](https://data140.org/textbook/content/chapter-09/probability-by-conditioning/): **The fundamentals: addition and multiplication rules, conditioning and Bayes' rule,** conditioning and recursion
- [Chapter 5](https://data140.org/textbook/content/chapter-05/collections-of-events/): Chances (or bounds on chances) of unions and intersections of several events, with major examples 

### Distribution ###
- **[Chapter 3](https://data140.org/textbook/content/chapter-03/random-variables/): Random variables, equality versus equality in distribution**
- **[Chapter 4](https://data140.org/textbook/content/chapter-04/relations-between-variables/): Joint, marginals, conditionals, independence**
- [Section 5.3.1](https://data140.org/textbook/content/chapter-05/the-matching-problem/#matches-at-fixed-locations) [Section 5.4](https://data140.org/textbook/content/chapter-05/sampling-without-replacement/): Random permutations and symmetry

### Expectation ###
- **[Chapter 8](https://data140.org/textbook/content/chapter-08/expectation/): The main properties, including additivity, the method of indicators, and expectations of functions (linear and non-linear), as well as the tail sum formula for the expectation of a non-negative integer valued variable**
- [Section 9.1](https://data140.org/textbook/content/chapter-09/expectation-by-conditioning/): Iterative expectation by conditioning

---

### Random Counts ###
These distributions are fundamental elements of discrete probabilistic modeling. **ALL of this section should be in bold.**
- [Section 8.1](https://data140.org/textbook/content/chapter-08/applying-the-definition/#bernoulli-and-indicators): Bernoulli
- [Section 8.2](https://data140.org/textbook/content/chapter-08/applying-the-definition/#uniform-on-an-interval-of-integers): Uniform on a, a+1, ... , b
- Sections [6.1](https://data140.org/textbook/content/chapter-06/binomial-distribution/), [6.3](https://data140.org/textbook/content/chapter-06/multinomial-distribution/), [8.5](https://data140.org/textbook/content/chapter-08/method-of-indicators/#expectation-of-the-binomial): Binomial, multinomial, expectation of the binomial
- Sections [5.4](https://data140.org/textbook/content/chapter-05/sampling-without-replacement/#counting-good-elements-in-a-simple-random-sample), [6.4](https://data140.org/textbook/content/chapter-06/the-hypergeometric-revisited/), [8.5](https://data140.org/textbook/content/chapter-08/method-of-indicators/#expectation-of-the-hypergeometric): Hypergeometric and its expectation
- Section [6.6](https://data140.org/textbook/content/chapter-06/law-of-small-numbers/), Lab 1, [Chapter 7](https://data140.org/textbook/content/chapter-07/poissonization/), Sections [8.2](https://data140.org/textbook/content/chapter-08/applying-the-definition/#poisson), [8.3](https://data140.org/textbook/content/chapter-08/expectations-of-functions/#e-x-x-1-for-a-poisson-variable-x), [8.4](https://data140.org/textbook/content/chapter-08/additivity/#e-x-2-for-a-poisson-variable-x): Poisson and related expectations
- Sections [8.2](https://data140.org/textbook/content/chapter-08/applying-the-definition/#geometric), [9.3](https://data140.org/textbook/content/chapter-09/expected-waiting-times/): Geometric, its right hand tail, and its expectation; related expected waiting times by conditioning

---

### Lab Sections in Scope
- **Lab 1:** The formula for the TVD is at the top of Section 1, but the key is 1b. Look carefully at the Poisson histogram in 2c, especially the modes; then study 3c for matching problem approximations. For binomial approximations, study 4a, 4c.
- **Lab 2:** First study the assumptions of the process, under *The Process* above Part A. See what happens as $\theta$ changes; look at 2d as well. Then study 1c, 4a, 4c.