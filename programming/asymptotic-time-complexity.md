# Asymptotic Time Complexity

During my datastructures classes in IIIT Kottayam, asymptotic time complexity was explained very well. I thought of writing the example he shared in the class:

`Consider if you are travelling from Kochi to New Delhi. You can reach the location:`

`by flight in 3 hours`

`by train in 2 days`

`by walking in 90 days`

So **big O notation**, can be such that the time required to walk is 90 days. It's considered as the upper bound such that f(n) <= cg(n).

In lowest possible time, let's say we can reach using flight. So it's the lower bound. Such that the f(n)>= c.g(n) always. It's considered **big theta notation**.

Then there is average case complexity which is means between both big O and big theta notation. It gives a tighter bound on run time such that. This is called **big theta notation** and can represented as follows

c1.g(n) <= f(n) <= c2.g(n)

We usually in industry consider even though it's considered as upper bound. It's usually considered closer to definition of big theta time.

![](<../.gitbook/assets/image (28).png>)
