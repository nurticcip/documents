---
tags: 
создал заметку: "2024-11-05"
---
### Краткое описание

```python
def solution(text, ending):
	return text.endswith(ending)
```


method endswith() - is used to check if a string ends with a specific substring. It returns `True` if the string ends with the specified substring, and `False` otherwise.

```python
string.endswith(suffix[, start[, end]])
```

- **suffix**: The substring you want to check for at the end of the string.
- **start** _(optional)_: The position in the string to start searching (default is the beginning).
- **end** _(optional)_: The position in the string to stop searching (default is the end of the string).


```python
def get_middle(s):
	l = len(s)
	m = l // 2
	if l % 2 == 0:
		return s[m - 1 : m + 1]
	else:
		return s[m]
get_middle('nur')
```


```python
def get_shortest_lenght(s):
	s = s.split()
	return min(len(i)for i in s)
```


