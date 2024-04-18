# Sort the odd
## Detail
You will be given an array of numbers. You have to sort the odd numbers in ascending order while leaving the even numbers at their original positions.

### Example
```
[7, 1]  =>  [1, 7]
[5, 8, 6, 3, 4]  =>  [3, 8, 6, 5, 4]
[9, 8, 7, 6, 5, 4, 3, 2, 1, 0]  =>  [1, 8, 3, 6, 5, 4, 7, 2, 9, 0]
```

## Answer
**My Solution**
```
def sort_array(source_array):
    odd_array = sorted([x for x in source_array if x % 2 == 1], reverse=True)
    odd = len(odd_array)
    for y, x in enumerate(source_array):
        if x % 2 == 1:
            odd -= 1
            source_array[y] = odd_array[odd]
            
    return source_array
```
**Alternate Solution**
```
def sort_array(arr):
  odds = sorted((x for x in arr if x%2 != 0), reverse=True)
  return [x if x%2==0 else odds.pop() for x in arr]
```