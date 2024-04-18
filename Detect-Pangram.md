# Detect Pangram
## Detail
A pangram is a sentence that contains every single letter of the alphabet at least once. For example, the sentence "The quick brown fox jumps over the lazy dog" is a pangram, because it uses the letters A-Z at least once (case is irrelevant).

Given a string, detect whether or not it is a pangram. Return True if it is, False if not. Ignore numbers and punctuation.

## Answer
**My Solution**
```
def delete_nth(order,max_e):
    result = []
    for num in order:
        if result.count(num) < max_e:
            result.append(num)
    return result
```
**Alternative Solution**
```
import string

def is_pangram(s):
    s = s.lower()
    for char in string.ascii_lowercase:
        if char not in s:
            return False
    return True
```