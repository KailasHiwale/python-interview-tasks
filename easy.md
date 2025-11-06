# Easy Interview Tasks


<details>
<summary><strong>Task 1</strong>  
    
Write a program to calculate factorial of a number recieved via console. Apply validation for invalid input and display appropreate message.  
    
Example 1 - Console input: 5, Output: 120  

Example 2 - Console input: "test", Output: Invalid number </summary>  

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
