---
layout: default
title: Probability Facts
---

<script>
window.MathJax = {
  tex: {
    tags: 'none'
  }
};
</script>
<script async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
<style>
.main {
  max-width: 1000px;
}

.fact-date {
  color: #666;
  font-size: 0.9em;
  margin-bottom: 0.2em;
}

.fact-block {
  margin: 1.4em 0 2em 0;
  padding-bottom: 1.1em;
  border-bottom: 1px solid #e2e2e2;
}

.fact-block p {
  text-align: justify;
  text-justify: inter-word;
  hyphens: auto;
}
</style>

# Probability: Interesting Facts

I have started to dive deep into probability theory. Sometimes I find something very interesting there that drives me crazy. To avoid annoying my girlfriend with it, I decided to keep these facts as a blog page on my personal website.

---

<div class="fact-block" markdown="1">
<div class="fact-date">2026-05-18</div>

## Number of fixed points in a random permuttation 

Lets consider all of the permuttations $S_n$ of $n$ elements. We define $X(\sigma)$ to be the number of the fixed points in a random permuttation $\sigma$ i.e. $\sigma(i) = i$. We want to find the expectation value $E[X(\sigma)]$.

Easy solution:

$$
E[X(\sigma)] = \frac{1}{n!} \sum_{\sigma} X(\sigma)
$$

We introduce the indicator function $$X(sigma) = \sum_{i=1}^n I_{\sigma(i) = i}$$. Then 

$$
\sum_{\sigma} X(\sigma) = \sum_{\sigma}\sum_{i=1}^n I_{\sigma(i) = i} = \sum_{i=1}^n\sum_{\sigma}I_{\sigma(i) = i} 
$$

It is easy since for the fixed $$i$$ $$\sum_{\sigma}I_{\sigma(i) = i} = (n-1)!$$, so we get 

$$
\sum_{\sigma} X(\sigma) = n (n-1)! = n!
$$
and $E[X(\sigma)] = 1$.

This is a very nice solution using the indicator function. There is also a straitforward one: 

$$
E[X(\sigma)] = \sum_{k = 0}^n k P(X = k)
$$

and $$P(X = k) = C_{n}^k D_{n-k}/n!$$ where $$D_{n}$$ - is the derangements (gives the number of permutations of n objects that leave no object fixed). It is called Subfactorial in Wolfram Mathematica. Wolfram code is pretty straightforward:3

```mathematica
n = 200;
Sum[k*Binomial[n, k]*Subfactorial[n - k]/Factorial[n], {k, 0, n}]
```

This computes the expectation value $$E[X(\sigma)]$$ for $$n = 200$$ elements as an example and gives 1 for any n.  

</div>
<div class="fact-block" markdown="1">
<div class="fact-date">2026-04-26</div>

## How Markov Chains Started

At the beginning of the 20th century, Andrey Markov wanted to challenge the idea that the law of big numbers only works for independent events.

To make the point convincing, he analyzed language data from Alexander Pushkin's poem *Eugene Onegin*. He took a long sequence of letters and labeled each one as either a vowel or a consonant.

If letters were independent, the chance of a vowel after a vowel would be the same as the overall vowel frequency. But Markov showed these transition frequencies were different: the next symbol depends on the current one.

In other words, he studied sequences where each next outcome depends on the current state, not on the full past. This was one of the first clear quantitative examples of dependence handled with probability theory.

This became the core idea of a Markov chain: memory is limited to the present state.

In formula form, the Markov property is

$$
\begin{aligned}
P(X_{n+1}=x_{n+1} \mid X_0=x_0, \ldots, X_n=x_n) \\
&= P(X_{n+1}=x_{n+1} \mid X_n=x_n).
\end{aligned}
$$

Why it matters: this simple rule is now used in physics, queueing theory, search ranking, genetics, and machine learning.

Historical note: Markov published this line of work in the 1900s, and the *Eugene Onegin* example became a classic story in probability courses because it turns abstract dependence into something concrete and intuitive.

I learned this story from an amazing Veritasium video: [Markov Chains](https://www.youtube.com/watch?v=KZeIEiBrT_w).

</div>

<div class="fact-block" markdown="1">
<div class="fact-date">YYYY-MM-DD</div>

## Title of your next fact

Write a short story or intuition.

Optional formula:

$$
\text{Put your equation here}
$$

Why it matters: add one sentence about applications.

</div>
