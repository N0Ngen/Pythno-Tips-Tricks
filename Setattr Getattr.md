# Setattr/Getattr

### Setattr
> The ```setattr()``` function sets the value of the specified attribute of the specified object.

##### Syntax

```python
setattr(object, attribute, value)
```

#### Parameter Values

| Parameter     | Description          |
| -------- | -------------- |
| object | ```Required``` An object. |
| attribute | ```Required``` The name of the attribute you want to set. |
| value | ```Required``` The value you want to give the specified attribute |

---

### Getattr
> The ```getattr()``` function returns the value of the specified attribute from the specified object.

##### Syntax

```python
getattr(object, attribute, default)
```

#### Parameter Values

| Parameter     | Description          |
| -------- | -------------- |
| object | ```Required``` An object. |
| attribute | The name of the attribute you want to get the value from. |
| default | ```Optional``` The value to return if the attribute does not exist. |

---
Example
### Set object attributs with ```serattr()```
```python
class Person():
    pass # Just create a ```Person``` class

person = Person() # ```person``` is an object/instance of ```Person``` class
```

- Dynamically add Attributes to ```person``` object

```python
class Person():
    pass # Just create a ```Person``` class

person = Person() # ```person``` is an object/instance of ```Person``` class

person.first = 'John'
person.last = 'Doe'
    
# Print attribute values
print(person.first)
print(person.last)
```

- Will produce

```python
John
Doe
```
> When the object attributes are values of some variables

```python
class Person():
    pass # Just create a ```Person``` class

person = Person() # ```person``` is an object/instance of ```Person``` class

# The attributes are values of some variables
first_key = 'first'
first_value = 'John'
```

> The ```Setattr()``` let us access the variables values.

```python
class Person():
    pass # Just create a ```Person``` class

person = Person() # ```person``` is an object/instance of ```Person``` class

# The attributes are values of some variables
first_key = 'first'
first_value = 'John'

# Setattr
setattr(person, first_key, first_value)

# Print the object attribute values
print(person.first)
```

- Will produce

```python
John
```

---

### Get object attributs with ```Gerattr()```

```python
class Person():
    pass # Just create a ```Person``` class

person = Person() # ```person``` is an object/instance of ```Person``` class

# The attributes are values of some variables
first_key = 'first'
first_value = 'John'


# Setattr
setattr(person, first_key, first_value)


# Getattr
first = getattr(person, first_key)

# Print the value
print(first)

```

- Will produce

```python
John
```

---

> Loop over a dictionary, add its keys as an object attributes,  and the dictionary values as an object attributes values.

```python
class Person():
    pass # Just create a ```Person``` class

person = Person() # ```person``` is an object/instance of ```Person``` class

# Object attributes and their values are dictionary keys & values.
person_info = {'first': 'John', 'last': 'Doe'}

# Loop over dictionary keys & values
for key, value in person_info.items():
    setattr(person, key, value)

# Print object attributes and their values    
print(person.first)
print(person.last)

# Get object attributes and their values with getattr and print them.
for key in person_info.keys():
    print(getattr(person, key))
```

- Will produce

```python
John
Doe
John
Doe
```