# ```*args **kwargs```

### ```*args```

> The special syntax ```*args``` in function definitions in python is used to pass a variable number of arguments to a function.
- The function will receive a tuple of arguments, and can access the items accordingly.

---

### ```**kwargs```

> The special syntax **kwargs in function definitions in python is used to pass a keyworded, variable-length argument list. 
- The function will receive a dictionary of arguments, and can access the items accordingly.

---

### Examples

```*args```

```python
# *args for variable number of arguments 
def myFun(*argv):  
    for arg in argv:  
        print (arg) 
    
myFun('Hello', 'Welcome', 'to', 'args')
```

- Will produce

```python
Hello
Welcome
to
args
```

##### ```*args``` with first extra argument

```python
def myFun(arg1, *argv): 
    print ("First argument :", arg1) 
    for arg in argv: 
        print("Next argument through *argv :", arg) 
  
myFun('Hello', 'Welcome', 'to', 'args')
```

- Will produce

```python
First argument : Hello
Next argument through *argv : Welcome
Next argument through *argv : to
Next argument through *argv : args
```

---

```**kwargs```

```python
# *kwargs for variable number of keyword arguments 
def myFun(**kwargs):  
    for key, value in kwargs.items(): 
        print ("%s == %s" %(key, value)) 

myFun(first ='Welcome', mid ='To', last='**Kwargs') 
```

- Will produce

```python
first == Welcome
mid == To
last == **Kwargs
```

#####  Variable number of ```**kwargs``` arguments with one extra argument.

```python
def myFun(arg1, **kwargs):  
    print(arg1)
    for key, value in kwargs.items(): 
        print ("%s == %s" %(key, value)) 

myFun("Hi", first ='Welcome', mid ='To', last='**Kwargs')
```

- Will produce

```python
Hi
first == Welcome
mid == To
last == **Kwargs
```

---

### Using ```*args``` and ```**kwargs``` to call a function.

```python
def myFun(arg1, arg2, arg3): 
    print("arg1:", arg1) 
    print("arg2:", arg2) 
    print("arg3:", arg3) 
      
# Now we can use *args or **kwargs to 
# pass arguments to this function :  
args = ("Welcome", "To", "*args") 
myFun(*args) 
  
kwargs = {"arg1" : "Welcome", "arg2" : "To", "arg3" : "**kwargs"} 
myFun(**kwargs)
```

- Will produce

```python
arg1: Welcome
arg2: To
arg3: *args
arg1: Welcome
arg2: To
arg3: **kwargs
```

##### Using ```*args``` and ```**kwargs``` in the same line to call a function


```python
def myFun(*args,**kwargs): 
    print("args: ", args) 
    print("kwargs: ", kwargs) 
  
  
# Now we can use both *args ,**kwargs to pass arguments to this function
myFun('Welcome','To','*args',first="Welcome",mid="To",last="**kwargs")
```

- Will produce

```python
args:  ('Welcome', 'To', '*args')
kwargs:  {'first': 'Welcome', 'mid': 'To', 'last': '**kwargs'}
```