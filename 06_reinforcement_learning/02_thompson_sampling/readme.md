# Thompson Sampling

## Introduction

- Thompson Sampling is a popular algorithm for decision-making under uncertainty in the field of reinforcement learning and probabilistic optimization. The algorithm is based on Bayesian statistics and is used to solve the exploration-exploitation dilemma that arises in decision-making problems.

- The basic idea of the Thompson Sampling algorithm is to maintain a posterior probability distribution over the unknown parameters of a model, and then use this distribution to guide the decision-making process. Specifically, the algorithm samples from the posterior distribution, and then chooses the action that is most likely to lead to the best outcome based on the samples.

- The algorithm is typically used in multi-armed bandit problems, where the goal is to find the arm with the highest expected reward among a set of arms with unknown reward distributions. In this case, Thompson Sampling starts by assuming a prior distribution over the reward distribution of each arm. Then, at each time step, it samples a reward distribution for each arm from its corresponding posterior distribution, and selects the arm with the highest expected reward based on the sampled distributions.

- The key advantage of Thompson Sampling is that it balances exploration and exploitation in a natural way, by sampling from the posterior distribution rather than simply choosing the arm with the highest observed reward. This allows the algorithm to effectively explore the space of possible actions while also exploiting the most promising options.

- Overall, Thompson Sampling is a powerful algorithm for decision-making under uncertainty, and has been shown to be effective in a wide range of applications, including online advertising, recommendation systems, and clinical trials.

---

## Algorithm

![Thompson Sampling](../../images/06_reinforcement_learning/Thompson_Sampling_Slide.png)

- We calulate the probability of each arm giving a reward using the `Beta Distribution`.

---

## `Thompson sampling generally outperforms the UCB algorithm`