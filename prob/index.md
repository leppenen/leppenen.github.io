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
</style>

# Probability: Interesting Facts

Add new facts at the top.
Date format: `YYYY-MM-DD`.
Keep each fact short and intuitive.

---

<div class="fact-block">
<div class="fact-date">2026-04-26</div>

## How Markov Chains Started

At the beginning of the 20th century, Andrey Markov wanted to challenge the idea that probability only works for independent events.

To make the point convincing, he analyzed language data from Alexander Pushkin's poem *Eugene Onegin*. He took a long sequence of letters and labeled each one as either a vowel or a consonant.

If letters were independent, the chance of a vowel after a vowel would be the same as the overall vowel frequency. But Markov showed these transition frequencies were different: the next symbol depends on the current one.

In other words, he studied sequences where each next outcome depends on the current state, not on the full past. This was one of the first clear quantitative examples of dependence handled with probability theory.

This became the core idea of a Markov chain: memory is limited to the present state.

In formula form, the Markov property is

$$
P(X_{n+1}=x_{n+1} \mid X_n=x_n, X_{n-1}=x_{n-1}, \ldots, X_0=x_0)
= P(X_{n+1}=x_{n+1} \mid X_n=x_n).
$$

Why it matters: this simple rule is now used in physics, queueing theory, search ranking, genetics, and machine learning.

Historical note: Markov published this line of work in the 1900s, and the *Eugene Onegin* example became a classic story in probability courses because it turns abstract dependence into something concrete and intuitive.

</div>

<div class="fact-block">
<div class="fact-date">YYYY-MM-DD</div>

## Title of your next fact

Write a short story or intuition.

Optional formula:

$$
\text{Put your equation here}
$$

Why it matters: add one sentence about applications.

</div>
