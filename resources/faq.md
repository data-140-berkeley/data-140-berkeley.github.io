---
layout: page
title: Frequently Asked Questions
nav_exclude: true
description: Frequently asked questions about important general issues.
---

{: .warning }
⚠️ The content on this site is archived and retained exclusively for reference. Updates will be made when the course if offered in the future.

# Frequently Asked Questions #
## Ani Adhikari, Spring 2017 ##
{:.no_toc .text-delta}

## Table of Contents
{: .no_toc .text-delta }

- TOC
{:toc}

## 1. What are they looking for when a question asks for the distribution of something?
**Answer:** "They" = me, and "something" = a random variable. I am asking you to specify, in any reasonable way, all the possible values of the variable as well as a rule for how the total probability of 100% is distributed over those values. Important steps, to be taken *always*:
- **Figure out the list of possible values before you calculate any probabilities.** This has a wonderful way of focusing the mind when you do start finding chances. It stops you making gross errors like saying continuous variables are discrete, or exponential variables are normal.
- After you've got the probabilities, try to make sure that they sum (or integrate) to $$1$$.

Ways to specify a distribution:
1. If you recognize the random variable as having one of the well-known distributions then you can simply specify by its name and parameters. E.g. "uniform on the integers $$1$$ through $$100$$", or "gamma with shape parameter $$r=5$$ and rate $$\lambda=1.9$$", etc. But your answer is incomplete if you just give the name of the distribution without values for the parameters. Be aware that in order to do this you have to thoroughly understand how all the different well-known distributions arise and interact with each other.
2. If the variable has finitely many values, make a distribution table showing all the possible values and their probabilities. Equivalently you can specify the probabilities in a formula which includes a clear statement about when (i.e. for which possible values) the formula is valid.
3. The cdf of any random variable specifies its distribution completely. Equivalently, the survival function specifies the distribution completely.
4. Distributions of continuous random variables can be specified in a variety of ways:
  - if it's a well-known distribution: its name and parameters
  - the possible values and the density
  - the possible values and the cdf
  - the possible values and the survival function

## 2. What's the difference between distribution, cdf, and density?
**Answer:** The distribution of a random variable is, always, the set of all possible values of the random variable and a clear specification of how the probabilities are distributed over those values (see [Question 1](http://prob140.org/resources/faq/#1-what-are-they-looking-for-when-a-question-asks-for-the-distribution-of-something)). The cdf is one way of specifying the distribution (see 1.3). If the random variable is continuous, the density is another way of specifying the distribution (see 1.1).

## 3. What are the different ways of finding a density? ##
**Answer:** Here are some of the most common ways of finding the density of a continuous random variable $$X$$. In many problems, one of these ways will turn out to be much more convenient than the others. Which one is most convenient will depend on the problem. No matter what method you use, identify the possible values first! 
1. See if you can recognize it as something well known. To do this you have to thoroughly understand how all the different well known densities arise and interact with each other. If you recognize it, give its name and say what its parameters are in the context of the problem.
2. If you can write $$X$$ as a nice function of a random variable whose density you know, use the change of variable formula for densities.
3. Find $$P(X \in dx)$$ and write it as $$(\text{function of } x) \times dx$$. The $$\text{function of } x$$ is the density.
4. Find the cdf of $$X$$ and differentiate.
5. If you know the joint density of $$X$$ and $$Y$$, you can find the density of $$X$$ by integrating the joint density over all the possible values of $$Y$$.

## 4. How do you find a joint distribution? ##
**Answer:** If the two variables are discrete you'll be finding a joint probability function. In the continuous case you'll be finding a joint density function. The main techniques:
1. Are the two variables independent? Then you can simply state the marginals and say the variables are independent. If you are required to find the joint distribution or the joint density, then multiply the marginals.
2. Joint distributions of discrete random variables can be specified in a table or by a formula for the joint probability function $$P(X=x, Y=y)$$ for all possible pairs $$(x,y)$$. You may be able to find the joint probability function directly from first principles or by conditioning and using the multiplication rule.
3. There are two cases which you should simply recognize:
  - Is the joint distribution uniform over a region? In that case the joint density or joint probability function is constant over the space of possible values.
  - Is the joint distribution bivariate normal? In that case you can simply fill in the blanks in, "bivariate normal, $$E(X) = ~~~~~~$$, $$E(Y) = \text{    }$$, $$Var(X) = \text{    }$$, $$Var(Y) = \text{    }$$, $$Corr(X,Y) = \text{    }$$,". Yes, you can specify SD instead of variance if you prefer; just say clearly which one you're listing.
4. If none of the above has worked, you can find a joint density from first principles. Specify the possible pairs $$(x,y)$$. Find $$P(X \in dx, Y \in dy)$$. The joint density is everything in that answer except the $$dxdy$$.
5. If even 4.4 hasn't worked, then find the density of one of the variables, say $$X$$, and multiply by the conditional density of $$Y$$ given $$X$$.

## 5. What are the different ways of finding expectations? ##
**Answer:** Treat the definition of the expectation of $$X$$ (multiply the possible values by their probabilities and then add; or multiply the possible values by the density and then integrate) as you treat the general definition of a derivative. Don't use it unless the random variable is really simple (e.g. an indicator or something with a tiny distribution table) or you have no other choice. Rather, start as follows:
1. Do you recognize the distribution of $$X$$? If it's one of the famous distributions, you can read $$E(X)$$ off the properties of the distribution.
2. Can you write $$X$$ as a sum? This one is crucial, because if you can write X as a sum (or difference, or other linear combination) of simpler variables whose expectations you know, then you can use additivity to find $$E(X)$$. The method of indicators is an important special case; see [Question 6](http://prob140.org/resources/faq/#6-how-do-i-know-to-use-indicators) below.
3. Is $$X$$ a nice function of some variable $$Y$$ which has a known distribution? In that case you can find $$E(X)$$ by using what you know about $$Y$$. If your function $$g$$ is linear, use linearity of expectation. If it's quadratic, use the appropriate combination of $$E(Y^2)$$ and $$E(Y)$$. For other functions $$g$$, find $$E(X) = E(g(Y))$$ by the function rule for expectations: multiply the values $$g(y)$$ by the density of $$Y$$ and then integrate with respect to $$y$$. Or, in the discrete case, multiply $$g(y)$$ by $$P(Y=y)$$ and then add over all $$y$$.
4. Can you condition on something useful? That is, does $$X$$ depend on a variable $$Y$$ in such a way that $$E(X \mid Y)$$ is a nice function of $$Y$$? If so, you can calculate $$E(X)$$ as $$E(E(X \mid Y))$$. Usually you can identify $$Y$$ like this: if you find yourself saying, "If I knew the value of this other random variable then I'd know the expectation of $$X$$," then "this other random variable" may be a good candidate for $$Y$$.
5. Can you use the tail sum formula? This method is not nearly as common as the others, but it is useful for positive integer-valued variables whose tail probabilities have a simple form. Typical examples are minima, maxima, and waiting times. Analogously, for positive continuous variables you can integrate the survival function to find the expectation.
6. If all else fails, or if the distribution of $$X$$ is really very simple, then plug in to the definition of expectation.

## 6. How do I know to use indicators? ##
**Answer:** The method is entitled "Method of indicators for expected counts". That's what it's for: to find the expected number of events that occur. It is also handy for finding variances of counts. See e.g. the derivation of the variance of the binomial. Sometimes these variances involve covariances as well. See e.g. the derivation of the variance in the matching problem and [Question 9](http://prob140.org/resources/faq/#9-so-then-what-are-the-different-ways-of-finding-covariances) below.

## 7. What are the different ways of finding SDs? ##
1. As always, start by seeing if the random variable has a well-known distribution. Then you can read the SD off known facts for that distribution.
2. See if the random variable is a linear function of another variable whose SD you know, and use linear change of variable for SDs.
3. If neither 7.1 nor 7.2 apply, then you almost invariably have to find the variance somehow and then take its square root. Which leads to the next question.

## 8. So then what are the different ways of finding variances? ##
Answer: As far as this course is concerned, the answers are essentially the same as those in parts 5.1, 5.2, 5.4, and 5.6 from [Question 5](http://prob140.org/resources/faq/#5-what-are-the-different-ways-of-finding-expectations)
1. (Same as 5.1) Do you recognize the distribution? If so, you can read off the variance. (Of course if you can recognize the distribution then you'll already have read off its SD directly, but I'm keeping the method here for completeness.)
2. (Same as 5.2) Can you write the variable as the sum of simpler variables? If so, the variance can be found as "the sum of all the variances as well as all the covariances" (see [Question 9](http://prob140.org/resources/faq/#9-so-then-what-are-the-different-ways-of-finding-covariances) below). An important special case is writing a count as a sum of indicators; see [Question 6](http://prob140.org/resources/faq/#6-how-do-i-know-to-use-indicators) above. Finally, if the variables in your sum are independent, then all the covariance terms are 0 and so the variance of the sum is just the sum of the variances.
3. (Same as 5.4) Can you condition on something useful? In that case, use $$Var(X) = E(Var(X \mid Y)) + Var(E(X \mid Y))$$. Or first find $$E(X)$$ by conditioning, then find $$E(X^2)$$ by conditioning, using the same method as for $$E(X)$$. Now use the computational formula $$Var(X) = E(X^2) - (E(X))^2$$.
4. (Same as 5.6) If 8.1, 8.2 and 8.3 fail, you have to use the computational formula and the distribution of $$X$$. Pray that the distribution is simple enough so that you can carry out the calculations.

The most common method is writing the variable as a sum of simpler variables. These may be dependent, in which case the variance of their sum will also involve their covariances.

## 9. So then what are the different ways of finding covariances? ##
1. Check for independence. If the two variables are independent then the covariance is $$0$$.
2. See if you can write at least one of $$X$$ or $$Y$$ as a linear combination of simpler variables, then use bilinearity of covariance. The most common linear combinations are sums and differences.
3. Check to see if you have $$Corr(X,Y)$$, $$SD(X)$$, and $$SD(Y)$$. Then you can use $$Cov(X,Y) = Corr(X,Y)SD(X)SD(Y)$$.
4. Check to see if you already know $$Var(X)$$, $$Var(Y)$$, and $$Var(X+Y)$$. Then you can find the covariance by solving
$$Var(X+Y) = Var(X) + Var(Y) + 2Cov(X,Y)$$.
5. If all else fails use the computational formula for covariance: $$Cov(X, Y) = E(XY) - E(X)E(Y)$$. A crucial special case is the covariance between two indicators: $$Cov(I_A, I_B) = P(AB) - P(A)P(B)$$.

A general warning: If you find yourself trying to compute $$E(XY)$$ and $$X$$ or $$Y$$ is not an indicator or something very simple with just a few possible values, Prof. Adhikari is willing to bet that you've failed to notice that you can use one of 9.1-9.4 above.