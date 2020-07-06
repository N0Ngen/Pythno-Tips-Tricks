# Zip

### Definition and Usage

> The ```zip()``` function returns a zip object, which is an iterator of tuples.

- Iterate through different two lists

```python
names = ['Peter Parker', 'Clark Kent', 'Wade Wilson', 'Bruce Wayne']
heroes = ['Spider Man', 'Super Man', 'Dead Pool', 'Bat Man']
for index, name in enumerate(names):
    hero = heroes[index]
    print(f'{name} is actually {hero}')
```

- Will produce

```python
Peter Parker is actually Spider Man
Clark Kent is actually Super Man
Wade Wilson is actually Dead Pool
Bruce Wayne is actually Bat Man
```
---
- iterate through different two lists with ```zip()``` function
```python
names = ['Peter Parker', 'Clark Kent', 'Wade Wilson', 'Bruce Wayne']
heroes = ['Spider Man', 'Super Man', 'Dead Pool', 'Bat Man']
for name, hero in zip(names, heroes):
    print(f'{name} is actually {hero}')
```

- Will produce

```python
Peter Parker is actually Spider Man
Clark Kent is actually Super Man
Wade Wilson is actually Dead Pool
Bruce Wayne is actually Bat Man
```