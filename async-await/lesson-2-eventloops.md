# Lesson 2- Eventloops

* call\_soon
* call\_later
* run\_forever - loops

![](<../.gitbook/assets/image (1).png>)

Select operations

Eventloops can run only one things at a time. There is usually a :

selector or proactor

Reactors - reacts based on notifications used by reactors

twisted calls eventloops

I/0 completion Ports - changes. In windows you can use proactors and selctors. In Unix you can use selectors

![](<../.gitbook/assets/image (7).png>)

Base\_events - consists of base events, yet there is only while loops there

![](<../.gitbook/assets/image (8).png>)

Python 3.5 implementation, then in \`_run_once\`

![](<../.gitbook/assets/image (9).png>)

Heart of heart of asyncio is select\_once method which calls the proactors and is having selector.select(timeout) method

![](<../.gitbook/assets/image (10).png>)

![](<../.gitbook/assets/image (12).png>)

![](<../.gitbook/assets/image (13).png>)



Uvloop for production, as it's doing a lot of magic and improvement in results. As it's fastest implementation with similar performance to NodeJS

Eventloop is just a normal function for handling netoworks requests and is used to handle callbacks. By what?

![](<../.gitbook/assets/image (14).png>)

Eventloop is not magical, it's just a loop which handles network events and executes as callbacks one by one. It can handle many networks events concurrently with a selector or a proactor. While it can handle many callback, but only run one callback at a time. Some callbacks, run and come again with a trick called traumpaline

callsoon, calllater is difficult to run. But it's usually run using coroutine. These coroutines make asynchrnous programs easy and magical
