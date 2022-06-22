---
layout: landing
---

# Fastai Learning

When does it overfit?



training\_loss > validation loss

and metrics sees no improvement



learn.fine\_tune()

* Does freeze
* Then `learn.fit_one_cycle`
* Unfreeze
* again `learn.fit_one_cycle`
