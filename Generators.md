# Generators
> ```generator functions``` are a special kind of function that return a lazy iterator. These are objects that you can loop over like a list. However, unlike lists, lazy iterators do not store their contents in memory.

### Normal for loop

```python
def square_numbers(nums):
    result = []
    for i in nums:
        result.append(i * i)
    return result
    
my_nums = square_numbers([1, 2, 3, 4, 5])
```

- Will produce

```python
[1, 4, 9, 16, 25]
```

### Generators

```python
def square_numbers(nums):
    for i in nums:
        yield(i * i)
        # yield keyword is what makes it a generator and its return a generator object

my_nums = square_numbers([1, 2, 3, 4, 5])
print(my_nums)
```

- Will produce

```python
<generator object square_numbers at 0x00000282A1326CF0>
# generators don't hold the entire result in memory, its yields one result at a time
```

---

##### use for loop to print generator object value

```python
def square_numbers(nums):
    for i in nums:
        yield(i * i)
        # yield keyword is what makes it a generator and its return a generator object

my_nums = square_numbers([1, 2, 3, 4, 5])

for  num in my_nums:
    print(num)
```

- Will produce

```python
1
4
9
16
25
```

##### Use list comprehension

```python
def square_numbers(nums):
    for i in nums:
        yield(i * i)
        # yield keyword is what makes it a generator and its return a generator object

my_nums = [x * x for x in [1, 2, 3, 4, 5]]
print(my_nums)
```

- Will produce

```python
[1, 4, 9, 16, 25]
```

##### Convert list comprehension to generator

```python
def square_numbers(nums):
    for i in nums:
        yield(i * i)
        # yield keyword is what makes it a generator and its return a generator object

my_nums = (x * x for x in [1, 2, 3, 4, 5])
print(my_nums)
```

- Will produce

```python
<generator object <genexpr> at 0x000001C2F78F5CF0>
```