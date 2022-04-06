# Nested functions exception handling

Original question asked in Real Python slack group:\


I have a question about chained exception handling method and how to return except conditions when I use it for one function which relies on another function. The code can be found below for more context:\
\
[https://gist.github.com/kurianbenoy/59bc813b535adc3a739f87dd4d4f4fb7](https://gist.github.com/kurianbenoy/59bc813b535adc3a739f87dd4d4f4fb7)\
\
It looks to me from answers I got from experienced folks in Real python, there are two ways to do this:

1. **In main function write try/except code and raise the exception from nested inner function**\
   ****\
   ****Hello this is my rewriten code which required a custom class in Python:\
   \
   \
   class ModelNotSupported(Exception):\
   &#x20;pass\
   \
   ****[**https://gist.github.com/kurianbenoy/346090c325dcf4f8f77ec3fbda3f0f99**](https://gist.github.com/kurianbenoy/346090c325dcf4f8f77ec3fbda3f0f99)****

****

1. ****

****

