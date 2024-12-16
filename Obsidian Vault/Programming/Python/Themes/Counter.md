```python
word = "mississippi"
counter = {}

for letter in word:
    if letter not in counter:
         counter[letter] = 0
     counter[letter] += 1

print(counter)



>>> {'m': 1, 'i': 4, 's': 4, 'p': 2}
```


solution with method get():

```python
word = "mississippi"
counter = {}

for letter in word:
     counter[letter] = counter.get(letter, 0) + 1

print(counter)




>>> {'m': 1, 'i': 4, 's': 4, 'p': 2}
```


solution using by defaultdict

```python 
from collections import defaultdict

word = "mississippi" counter = defaultdict(int)
for letter in word:
	counter[letter] += 1

print(counter)



>>> defaultdict(<class 'int'>, {'m': 1, 'i': 4, 's': 4, 'p': 2})
```

