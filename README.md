# User-Defined-Functions
User defined functions which mimic map, filter and reduce in python.

### map()
```
def my_map(func,l):
    temp = []
    for i in range(len(l)):
        temp.append(func(l[i]))
    return temp
```

### filter()
```
def my_filter(func,l):
    temp = []
    for i in range(len(l)):
        if func(l[i]):
            temp.append(l[i])
    return temp
```

### reduce()
```
def my_reduce(func,l):
    temp = l.copy()
    while True:
        if len(temp) == 1:
            break
        temp[1] = func(temp[0],temp[1])
        temp.pop(0)

    return temp[0]
 ```
