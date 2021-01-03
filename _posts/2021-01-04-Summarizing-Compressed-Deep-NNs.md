---
title: "Summarizing 'What Do Compressed Deep Neural Networks Forget?'"
tag: Data Science
author_profile: true
toc: true
header:
  teaser: https://miro.medium.com/max/770/1*9onqVYdPPrCcwDX6mGKCpg.jpeg
  og_image: https://miro.medium.com/max/770/1*9onqVYdPPrCcwDX6mGKCpg.jpeg
---

["What do Compressed Deep Neural Networks Forget" by Sara Hooker and others](https://arxiv.org/pdf/1911.05248.pdf) is 2020 published [Arxiv.org](https://arxiv.org/) article ([also found here](https://weightpruningdamage.github.io/)) discusses the tradeoffs between optimization and improvements into "AI". Particularly, the article discusses how Deep Network "Pruning" results in  higher level "AI" performance, but with an underlying tradeoff is memorization of said model's __particular__ data points, what are ultimately called [Pruning Identified Exemplars (PIEs)](https://weightpruningdamage.github.io/#:~:text=natural%20adversarial%20images.-,PIE%3A%20Pruning%20Identified%20Exemplars,pruned%20and%20non%2Dpruned%20models.).

## Why should I be interested in this?

There should be a caution of using such optimizations for "AI" models as they can have societal impact on sensitive industries such as hiring, health care diagnostics, self-driving cars, facial recognition software, and others with small corner cases (i.e. uncommon occurrences).

You may be thinking, "ya okay, what's a real example of this?". Well, using programmatic implementations like Machine Learning or Artificial Intelligence, we can see consequences such as the following situations:
* [scaling up bias in hiring practices](https://www.reuters.com/article/us-amazon-com-jobs-automation-insight/amazon-scraps-secret-ai-recruiting-tool-that-showed-bias-against-women-idUSKCN1MK08G)
* Automated cars failed recognition in ultimately killing someone
* and other use cases

Now technically, you should be interested in this is that such pruning or optimizations to models in products affects __the compression impairs the model's ability to predict accurately on the long-tail of less frequent instances__.

## What's in the publication?

1. Abstract
2. Problem Statement
3. Testing Framework
4. Results
5. Comments, mentions, and mentions of related work in the data space

## Takeaways

Deep Learning Pruning is accepted by the industry because of optimizations in memory, energy consumption, and lower inference latency with having little degradation to test set accuracy. "However, this measure of performance conceals significant difference in how different" small subset of data, [Pruning Identified Exemplars (PIEs)](https://weightpruningdamage.github.io/#:~:text=natural%20adversarial%20images.-,PIE%3A%20Pruning%20Identified%20Exemplars,pruned%20and%20non%2Dpruned%20models.), are impacted by compression techniques.


> Side note: "What are Pruning Identified Exemplars (PIEs)?"
> From the article, "PIEs are images where there is a high level of disagreement between the predictions of pruned and non-pruned models."

These PIEs are corner cases, or uncommon occurrences, do not get classified correctly in a statistically significant implementation, for larger different degrees of pruned models.

And we should not some things about PIEs too, like the following:
* Mislabelled ("Ground Truth Label incorrect")
* Lower Quality or Corrupt Image
* Depict Multiple Objects
* Abstract Representations
* Require more fine-grained classifications (e.g. 'Green Bottle' vs 'Green Plastic Bottle')

Ultimately, as people in the data community create more complex & larger data models, we observe vulnerabilities in classification with "lower end-tail" of the distributions of classes $c \in C$. Moreover, PIEs are heavily over-indexed relative to non-PIEs on both __noisy__ (corrupted information) and __atypical__ (abstract representation) examples.

Again, this was a short summary. But if you want to read more about this, check out the [website](https://weightpruningdamage.github.io/) & [article](https://arxiv.org/pdf/1911.05248.pdf) on "Selective Brain Damage: Measuring the Disparate Impact of Model Compression"