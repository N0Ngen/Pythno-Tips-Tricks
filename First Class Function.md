# First Class Functions

##### ```First Class Functions```
> In computer science, a programming language is said to have first-class functions if it treats functions as first-class citizens. This means the language supports passing functions as arguments to other functions, returning them as the values from other functions, and assigning them to variables or storing them in data structures.

##### ```First Class Citizen```

> In programming language design, a first-class citizen in a given programming language is an entity which supports all the operations generally available to other entities. These operations typically include being passed as an argument, returned from a function, modified, and assigned to a variable.

### Examples

```python
def square(x):
    return x * x

f = square(5)
# Assign the result of the function to 'f'
print(quare) # Print the function 'square'
print(f) # Print the 'f' value
```

- Will produce

```python
<function square at 0x000001DBDB127CA0>
25
```

---

#### Treat variable as functions

```python
def square(x):
    return x * x

f = square # Set the var 'f' equal to the 'square' function
print(square)
print(f)
```

- Will produce

```python
<function square at 0x0000026DB0547CA0>
<function square at 0x0000026DB0547CA0>
```

```python
print(square(5))
print(f(5))
```

- Will produce

```python
25
25
```

---

#### Pass function as an argument to another function

```python
def square(x):
    return x * x
    
def my_map(func, arg_list):
    result = []
    for arg in arg_list:
        result.append(func(arg))
    return result
    
squeares = my_map(square, [1, 2, 3, 4, 5])
print(squeares)
```

- Will produce

```python
[1, 4, 9, 16, 25]
```

---

#### Return function from another function

```python
def logger(msg):
    
    def log_message():
        print('log: ', msg)

    return log_message
    
log_hi = logger('Hi')
log_hi()
```

- Will produce

```python
log:  Hi
```

```python
def html_tag(tag):

    def wrap_text(msg):
        print('<{0}>{1}</{0}>'.format(tag, msg))

    return wrap_text

print_h1 = html_tag('h1')
print_h1('Test Headline!')
print_h1('Another Headline!')

print_p = html_tag('p')
print_p('Test Paragraph!')
```

- Will produce

```python
<h1>Test Headline!</h1>
<h1>Another Headline!</h1>
<p>Test Paragraph!</p>
```