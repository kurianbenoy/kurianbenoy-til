# Extracting a Json Object as List(regex)

I had a JSON data like this:



"\[{'3': 'test'}, {'4': 'testathira'}, {'5': 'Sample Test'}, {'6': 'XYZ'}]



I want to write a regex statement to get these object in array of the nested JSON object into python list:



Let's check regex101 with website:

[https://regex101.com/r/0OhB7x/1/](https://regex101.com/r/0OhB7x/1/)



![](<../.gitbook/assets/image (31) (1).png>)



To write pythonic code for the following:

```
import re
x = input()
re.findall(r"{'[0-9]+': '[a-z][A-Z]+'}", x)
```

