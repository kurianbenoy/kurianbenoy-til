# HTTP Methods

HTTP defines a set of **request methods** to indicate the desired action to be performed for a given resource.



TRACE - The `TRACE` method performs a message loop-back test along the path to the target resource.\
\
Check: [https://www.blackhillsinfosec.com/three-minutes-with-the-http-trace-method/](https://www.blackhillsinfosec.com/three-minutes-with-the-http-trace-method/)

Other HTTP Methods are:



GET\
POST

PUT

PATCH

PUT is expecting full resource details to modify, while PATCH is expecting with partial details itself to modify stuff

OPTIONS



Using Get request with payload is not a good practise for client applications like in frontend websites, while in RFC protocol nothing is stopping from using that approach.
