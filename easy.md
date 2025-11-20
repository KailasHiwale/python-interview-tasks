# Easy Interview Tasks

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
    
Write a program to calculate factorial of a number recieved via console. Apply validation for invalid input and display appropreate message.  
    
Example 1: Console input: 5, Output: 120  

Example 2: Console input: "test", Output: Invalid number </summary>  

<strong>Solution</strong>

```python
def fact(n):
    if n<0:
        return f"Invalid value"
    elif n == 0:
        return 1
    return n * fact(n - 1)


try:
    n = int(input("Enter a number: "))
except Exception as e:
    print(f"Invalid value")
else:
    print(fact(n))
```
</details>

<details>  
    
<summary><strong>Task 2</strong>  
    
Write a program to remove vovels from givan string  

Example 1: input = "Life is beautiful", output = "Lf s btfl"

Example 2: input = "World Health Organisation" output = "Wrld Hlth rgnstn"</summary>  


<strong>Solution</strong>  


```python
input = "World Health Organisation"

output = ''.join([char for char in input if char.lower() not in "aeiou"])

print(output)
```
</details>

<details>  
    
<summary><strong>Task 3</strong>  
    
From a given list, fetch single frequency elements.    

Example 1: input: [1, 2, 2, 3, 3, 4, 4]    output: [1]</summary>  


<strong>Solution</strong>  


```python
l = [1, 2, 2, 3, 3, 4, 4]

freq = {}

for i in l:
    freq[i] = freq[i] + 1 if i in freq else 1

single_freq = [k for k in freq if freq[k] == 1]

print(single_freq)
```
</details>
