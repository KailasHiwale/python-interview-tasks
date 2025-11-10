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

<details>  
    
<summary><strong>Task 2</strong>  
    
Write a python code which accepts array as an inputs and find nth largest nos without using sorting function.    

Example 1  
input: [4, 2, 9, 8, 3], nth_larget = 2  
output: 8 </summary>  


<strong>Solution</strong>  


```python
def merge(left, right, lst):
    len_left, len_right, i, j, k = len(left), len(right), 0, 0, 0

    while i < len_left and j < len_right:
        if left[i] <= right[j]:
            lst[k] = left[i]
            i += 1
        else:
            lst[k] = right[j]
            j += 1
        k += 1

    while i < len_left:
        lst[k] = left[i]
        i += 1
        k += 1

    while j < len_right:
        lst[k] = right[j]
        j += 1
        k += 1

    return lst


def sort(lst):
    n = len(lst)
    if n < 2: return lst
    MID = n // 2
    left_half = sort(lst[:MID])
    right_half = sort(lst[MID:])
    return merge(left_half, right_half, lst)


def find_nth_largest(lst, nth):
    lst_sort = sort(lst)[::-1]
    return lst_sort[nth-1]
        

if __name__ == "__main__":
    lst = list(map(
        int, input("Enter space seperated list\n").rstrip().split()))
    nth = int(input("Enter number: "))
    print(find_nth_largest(lst, nth))
```
</details>
