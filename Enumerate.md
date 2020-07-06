# Enumerate
- With ```for``` loop.
```python
index = 0
names = ['Chris', 'Dave', 'Traves', 'Corey']
for name in names:
    print(f'{index} {name}')
    index += 1
```
- Will produce
```python
0 Chris
1 Dave
2 Traves
3 Corey
```
---
- With ```Enumerate```.
```python
names = ['Chris', 'Dave', 'Traves', 'Corey']
for index, name in enumerate(names): # Add optional ```Start``` parameter to Start from a specific number
    print(f'{index} {name}')
```
- Will produce
```python
0 Chris
1 Dave
2 Traves
3 Corey
```