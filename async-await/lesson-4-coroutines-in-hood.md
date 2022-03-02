# Lesson 4- coroutines in hood

Future object can report whether the object is actually being completed or really done

![](<../.gitbook/assets/image (3).png>)

* It's called the promises, deferred in other languages

We looked at about awaitables in asyncio

* coroutines
* tasks
* futures

On looking code implementation of coroutines, it's just simply a generator function. Learned about generators properties like next, fstate etc.

coroutine is just a normal generators, while tasks also doesn't have anything special.

The special functionality is implemented actually really in tasks, where it's calling a loop which calls one callback to another with multiple send loops

![](<../.gitbook/assets/image (22).png>)



In python3, the default implementation is in C, while python implementation is there which is exactly copied in C as well.

**Most common pitfall in asyncio**

****

![](<../.gitbook/assets/image (23).png>)



![](<../.gitbook/assets/image (25).png>)

Forgetting await with coroutiens. Using type hinting



![](<../.gitbook/assets/image (26).png>)

Holding long task, the blocking should never happen in asyncio

Network lattency in servers. When running 1000 asyncio clients, it's better handling than in other ways.

****
