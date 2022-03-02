# Python async/await

#### References

* [https://www.aeracode.org/2018/02/19/python-async-simplified/](https://www.aeracode.org/2018/02/19/python-async-simplified/)
* [https://docs.python.org/3/library/asyncio.html](https://docs.python.org/3/library/asyncio.html)
* [https://docs.python.org/3/library/asyncio-task.html](https://docs.python.org/3/library/asyncio-task.html)

On the plus side, nothing else can run while your code is moving through from one await call to the next, making race conditions harder.

This is called cooperative multitasking, and while it has many upsides, this silent failure mode is its main design issue. If you use a blocking synchronous call by mistake, nothing will explicitly fail, but things will just run mysteriously slowly.
