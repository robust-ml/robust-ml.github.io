---
layout: narrow
title: FAQ
---

# FAQ

## What are adversarial examples?

[Szegedy et al. (2013)](https://arxiv.org/abs/1312.6199) and [Biggio et al.
(2013)](https://arxiv.org/abs/1708.06131) showed that machine learning models
are vulnerable to adversarial examples, slightly perturbed inputs that cause
misclassification. There are lots of nuances, but that's the general idea. This
[blog post](https://blog.openai.com/adversarial-example-research/) by OpenAI is
a nice introduction to the topic.

## Why does this page exist?

Security is often a cat-and-mouse game. The purpose of this page is to help
researchers keep track of which defenses exist and which ones are broken. A
broken defense can no longer be considered "state-of-the-art", and it should
not be described in literature as a working defense against adversarial
examples without mentioning that it's broken.

## Which defenses are included?

The list includes published defenses for the white-box threat model that have
either made source code available or are broken.

## How do I submit an update / correction?

This website is open-source. Please open an
[issue](https://github.com/adversarial-defenses/adversarial-defenses.github.io/issues)
or submit a [pull
request](https://github.com/adversarial-defenses/adversarial-defenses.github.io/pulls)
with your proposed change.

## How is this list maintained?

This is a community-maintained document, open-source on
[GitHub](https://github.com/adversarial-defenses/adversarial-defenses.github.io).
All updates to the site are
[auditable](https://github.com/adversarial-defenses/adversarial-defenses.github.io/commits/master),
and all discussions related to content are also publicly visible (as GitHub
issues / pull requests).
