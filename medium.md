# Medium Interview Tasks

### Task 1. Write a program to flatten a nested list without using recusion.
Example -
Input: [1,[2,[3,4],5]]
Output: [1, 2, 3, 4, 5]

Solution:
```python
result = []
stack = l[:]

while stack:
    item = stack.pop(0)
    if isinstance(item, list):
        stack = item + stack
    else:
        result.append(item)
        
print(result)
```
