# Medium Interview Tasks

<details>  
    
<summary><strong>Task Template</strong>  
    
Add task statement here  

Example 1: add here

Example 2: add here </summary>  


<strong>Solution</strong>  


```python
# Python code here
```
</details>

<details>  
    
<summary><strong>Task 1</strong>  
    
Write a program to flatten a nested list without using recusion.  

Example 2: input = [1, [2, [3, 4], 5]], Output = [1, 2, 3, 4, 5] </summary>  


<strong>Solution</strong>  


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
</details>
