---
layout: narrow
title: FAQ
---

# FAQ

## Which defenses are included?

Currently, we list defenses that are claimed to be secure in the white-box
model. Defenses that only aim to be secure in an oblivious attacker / black-box
/ grey-box model, but not in a white-box model, are out of scope. It is unclear
how to properly evaluate such defenses, as it is challenging to model lack of
awareness of a defense (or part of a defense) being in place. In the future, we
may expand to include more threat models.

Defenses must also have open-source code available, along with pre-trained
models. Public availability of defenses enables third parties to more easily
perform security analyses. In the absence of first-party implementations, we
accept third-party implementations. If a first-party implementation for a
listed defense becomes available, please [let us know][issues] (or submit a
[pull request][pulls] with the update).

Defenses must also implement the [robustml API][robustml]. Implementing the
interface requires minimal additional effort, and it enables straightforward
evaluation of attacks.

We maintain two lists: one for [published defenses][defenses] and one for
[unpublished defenses][preprints]. Both contain defenses for the white-box
threat model that are open-source, implement the robustml API, and have
pre-trained models available.

## How are new defenses added to the list?

Defenses must be open-sourced, implement the robustml API, and have a
pre-trained model available to be eligible to be added to the list. See
[here][instructions] for instructions. Please submit a [pull request][pulls] to
add a new defense to the list.

By default, we list a single claim from the paper (for the “largest” dataset).
Authors can list up to 3 claims, with a single claim allowed for a (dataset,
threat model) pair.

## Why is defense X missing?

The defense is either not open-sourced or no one has implemented the [robustML
API][robustml] yet. Since this is a community-run website we can't expect it to be 100%
complete. Maybe you can implement the defense and/or the API and add it to the list!

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
(currently MNIST, Fashion-MNIST, CIFAR-10, GTS, and ImageNet ILSVRC 2012). If
you wish to add a new dataset, please open an [issue][issues].

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

## How is this different from the other existing resources on robust ML?

[CleverHans][cleverhans] is a library providing open-source implementations of
various known attack methods. This is an important resource that provides us
with a broad set of tools useful in working on robust ML. However, the key goal
of robust-ml.org, reflecting the current progress on key datasets and threat
models, is not a part of CleverHans's focus.

[robust.vision][robust vision] maintains a comparison between existing defenses
by evaluating each one of them against all currently known attacks. This
provides a useful overview of the relative power of known attacks and defenses.
However, due to its focus on evaluating defenses only on known, static attacks,
it might not necessarily reflect the actual progress on the defense front.
After all, defenses often appear effective by resisting all previously known
attacks but can be completely bypassed by new, adaptive ones.

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
[cleverhans]: https://github.com/tensorflow/cleverhans
[robust vision]: https://robust.vision/
