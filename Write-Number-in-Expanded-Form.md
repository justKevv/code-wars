# Write Number in Expanded Form
## Detail
You will be given a number and you will need to return it as a string in Expanded Form. For example:
```
expandedForm(12); // Should return '10 + 2'
expandedForm(42); // Should return '40 + 2'
expandedForm(70304); // Should return '70000 + 300 + 4'
```
NOTE: All numbers will be whole numbers greater than 0.

## Answer
**My Solution**
```
def expanded_form(num):
    return " + ".join([(str(num)[x] + "0" * (len(str(num)) - 1 - x)) for x in range(len(list(str(num)))) if str(num)[x] != "0"])
```
**Best Solutions**
```
def expanded_form(num):
    num = list(str(num))
    return ' + '.join(x + '0' * (len(num) - y - 1) for y,x in enumerate(num) if x != '0')
```
