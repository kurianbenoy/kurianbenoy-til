# Better to pass callback in fit\_one\_cycle

It’s better to pass callbacks to fine\_tune() and fit\_one\_cycle() method instead of passing directly to the learner object, to avoid unwanted effects when using your models for inferencing. I found this solution from one of the posts written by Wayde Gilliam.

{% embed url="https://forums.fast.ai/t/is-there-anyway-to-call-learn-get-preds-without-triggering-any-of-the-callbacks/64753/10" %}
