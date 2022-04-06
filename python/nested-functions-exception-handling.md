# Nested functions exception handling

Original question asked in Real Python slack group:\


I have a question about chained exception handling method and how to return except conditions when I use it for one function which relies on another function. The code can be found below for more context:\
\
[https://gist.github.com/kurianbenoy/59bc813b535adc3a739f87dd4d4f4fb7](https://gist.github.com/kurianbenoy/59bc813b535adc3a739f87dd4d4f4fb7)\
\
It looks to me from answers I got from experienced folks in Real python, there are two ways to do this:



**In main function write try/except code and raise the exception from nested inner function**\
****\
****Hello this is my rewriten code which required a custom class in Python:\
\
`py`\
`class ModelNotSupported(Exception):`\
&#x20;`pass`\
``\
``\
``\
``\
``****[**https://gist.github.com/kurianbenoy/346090c325dcf4f8f77ec3fbda3f0f99**](https://gist.github.com/kurianbenoy/346090c325dcf4f8f77ec3fbda3f0f99)****

```
supported = ["a", "b", "c", "en", "ta"]


def load_model(source, target):
    if source == target:
        raise ModelNotSupported("Hello how are you")
    if source in supported:
        if source == "en":
            return ("t", "t")
        else:
            raise ModelNotSupported("Language pair not available")


def predict_raw():
    try:
        tokenizer, model = load_model("en", "hello")
        return model
    except ModelNotSupported as e:
        return {"inputerror": e}
```

****

**This can be be implemented with a function which returns messages, and based on which return based on the conditions.**

```
```

