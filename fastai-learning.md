---
layout: landing
---

# When does overfitting happening in fast.ai?

Having a low training loss but high validation loss does not necessarily mean that your model is already overfitting. This is a point of confusion for most of us when starting out and trying to understand these ideas.

As mentioned in the book; when the validation set accuracy stops getting better, and instead goes in the opposite direction and gets worse, that is when you can start thinking that the model is starting to memorize the training set rather than generalize, and has started to overfit.
Taken straight from the book, Chapter 1 :

![image](https://user-images.githubusercontent.com/24592806/175348582-34fd36be-ee9d-4df8-897c-2e8d11f33580.png)


In other words, as you progress further on the training, once the validation loss starts getting consistently worse than what it was before, (and hence meaning that it’s not able to generalize as well to unseen data, while getting better on training data) then the model has started to overfit.

Not to be taken as an exact example, but I’ve tried to quickly sketch out what this could mean in practice.

![image](https://user-images.githubusercontent.com/24592806/175348697-713c69ac-a0d9-4fa8-8de5-c39dc77b2c1d.png)


and metrics sees no improvement

Source: https://forums.fast.ai/t/lesson-2-official-topic/96033/226?u=kurianbenoy
