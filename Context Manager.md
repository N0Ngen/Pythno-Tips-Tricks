# Context Manager
___
### Files
- Without Context Manager.
```python
source = 'file_name.txt'
open(source, 'mod') as f:
    file_content = f.read()
f.close()
```
- With Context Manager.
```python
source = 'file_name.txt'
with open(source, 'mod') as f:
    file_content = f.read()
```
___