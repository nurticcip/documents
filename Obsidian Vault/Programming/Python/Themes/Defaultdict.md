# How does defaultidc work?
When a `defaultdict` is created, you specify a factory function that will provide the default value for new keys. This factory function could be `int`, `list`, `str`, or any other callable object.

For example:

- **Using int:**  If you use `int` as the factory function, the default value will be 0 (since `int()` returns 0).
```Python
	from collections import defaultdict

	count_dict = defaultdict(int)

	text = "hello"

	for i in text:
	
		count_dict[i] += 1
		
	print(count_dict)



	Output >> 
	defaultdict(<class 'int'>, {'h': 1, 'e': 1, 'l': 2, 'o': 1})
```

- **Using list:** If you use `list` as the factory function, the default value will be an empty list (`[]`)
```Python
	from collections import defaultdict
	
	grouped_data = defaultdict(list)
	
	data = [("fruits", "apple"), ("fruits", "banana"),
	("vegetables", "carrot"), ("fruits", "orange"),
	("vegetables", "spinach")]
	
	for category, item in data:
	
		grouped_data[category].append(item)
		
	print(grouped_data)



	Output >> 
	defaultdict(<class 'list'>, {'fruits': ['apple',
	'banana', 'orange'], 'vegetables': ['carrot', 'spinach']})
```

- **Using  str:** If you use `str`, the default value will be an empty string (`''`)
```Python 
	from collections import defaultdict

	concatenated_data = defaultdict(str)

	data = [("greeting", "Hello"), ("greeting", " world"),
	("farewell", "Goodbye"), ("greeting", "!")]

	for key, value in data:
	
		concatenated_data[key] += value
		
	print(cocetenated_data) 
	



	Output >> 
	defaultdict(<class 'str'>, {'greeting': 'Hello world!',
	'farewell': 'Goodbye'})
```



