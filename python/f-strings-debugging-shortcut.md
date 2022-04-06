# f-strings debugging shortcut

Instead of typing things, with it's value twice. With f-strings there is a nice shortcut.



**Without f-strings:**\


```
number = 32
print(f"number={number}")

cards = {'R':4, 'J': 24}
print("cards", cards)
```

**With fstrings**

```
 print(f"{number = }")
 # returns number = 32
 print(f"{cards = }")
# returns cards {'R': 4, 'J': 24}
```
