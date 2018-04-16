---
layout: narrow
title: FAQ
---

# FAQ

## Which defenses are included?

We maintain two lists: one for [published defenses][defenses] and one for
[unpublished defenses][preprints]. Both contain defenses for the white-box
threat model that have open source code that implements the [robustml
API][robustml].

In the absence of first-party implementations, we accept third-party
implementations. If a first-party implementation for a listed defense becomes
available, please [let us know][issues] (or submit a [pull request][pulls] with
the update).

## How are new defenses added to the list?

Defenses must be open-sourced and implement the robustml API to be eligible to
be added to the list. See [here][instructions] for instructions. Please submit
a [pull request][pulls] to add a new defense to the list.

By default, we list a single claim from the paper (for the “largest” dataset).
Authors can list up to 3 claims, with a single claim allowed for a (dataset,
threat model) pair.

## How are analyses chosen?

We list all analyses that [implement the robustml attack interface][attack] to
attack the defense and respect the threat model of the paper. Because we
require both defenses and analyses to implement the robustml interfaces, they
can be easily [run][run] against each other.

## How are threat models chosen?

The threat models listed correspond to models [defined in the robustml
framework][threat models] and are based on models considered in published
papers. If you wish to add a new threat model, please open an [issue][issues].

## Which datasets are considered?

We include the datasets [defined in the robustml framework][datasets]
(currently MNIST, CIFAR-10, and ImageNet ILSVRC 2012). If you wish to add a new
dataset, please open an [issue][issues].

## Why only vision?

We currently only list defenses for computer vision because it is the most well
studied setting as of now. Consequently, this is a natural domain for comparing
various methods. We are, however, open to - and, in fact, encourage - work in
formal threat models corresponding to other ML settings. If you have new ideas
for threat models and datasets to include for non-vision defenses, please open
an [issue][issues].

## How do I submit an update?

This website is [open-source][source]. Please open an [issue][issues] or submit
a [pull request][pulls] with proposed changes.

## How is this website maintained?

This is a community-maintained website, open-source on [GitHub][source]. All
updates to the site are [auditable][commits], and all discussions related to
content are also publicly visible (as GitHub [issues][issues] / [pull
requests][pulls]).

[source]: https://github.com/robust-ml/robust-ml.github.io
[commits]: https://github.com/robust-ml/robust-ml.github.io/commits/master
[defenses]: /defenses/
[preprints]: /preprints/
[robustml]: https://github.com/robust-ml/robustml
[instructions]: https://github.com/robust-ml/robustml#usage
[issues]: https://github.com/robust-ml/robust-ml.github.io/issues
[pulls]: https://github.com/robust-ml/robust-ml.github.io/pulls
[threat models]: https://github.com/robust-ml/robustml/blob/master/robustml/threat_model.py
[datasets]: https://github.com/robust-ml/robustml/blob/master/robustml/dataset.py
[attack]: https://github.com/robust-ml/robustml/blob/master/robustml/attack.py
[run]: https://github.com/robust-ml/robustml/blob/master/robustml/evaluate.py
