# ```Closure```

> In programming languages, a closure, also lexical closure or function closure, is a technique for implementing lexically scoped name binding in a language with first-class functions. Operationally, a closure is a record storing a function together with an environment.

### Examples

```python
def outer_function():
    message = 'Hi' # 'message' is free variable cuz we didn't define it in 'inner_function' but still can accsess it
    def inner_function():
        print(message)
    return inner_function() # return the execution of the 'inner function'
    
outer_function()
```

- Will produce

```python
Hi
```

##### return inner_function

```python
def outer_function():
    message = 'Hi' # 'message' is free variable cuz we didn't define it in 'inner_function' but still can accsess it
    def inner_function():
        print(message)
    return inner_function # return the 'inner function'
    
my_func = outer_function() # 'my_function' is now actually a function and equal to 'inner_function'
print(my_func)
my_func()
```

- Will produce

```python
<function outer_function.<locals>.inner_function at 0x000001F0B2517D30>
```

```python
print(my_func)
my_func()
```

- Will produce

```python
<function outer_function.<locals>.inner_function at 0x0000026F27E27D30>
Hi
```

> So A ```closure``` is an inner Function that remember and has access to vars in the local scope in which it was created even after the outer function has finished executing.

```python
def outer_func(msg):
    message = msg
    def inner_func():
        print(message)
    return inner_func
    
hi_func = outer_func('hi')
hello_func = outer_func('hello')

hi_func()
hello_func()
```

- Will produce

```python
hi
hello
```
