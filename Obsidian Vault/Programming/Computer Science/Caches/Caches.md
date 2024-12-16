
**Cache** - used to optimize data transfers between any system elements with different characteristics (используется для оптимизации перпедачи данных между любыми элементами)

Difference between MEMORY and CACHE:
	Memory: 
		Slower, larger, cheaper 
		Partition into 'block'
	Cache:
		Smaller, faster, more expensive
		Stores a subset of blocks from memory
		Data is copied in block-sized chunks


Cache mechanics:
	Hit:
		Data we need is in block *b*, block *b* is in the cache. Data is returned to the CPU
	Miss:
		Data we need is in block *b*, block *b* is not in the cache already. Block *b* is written into the cache 


Cache takes advantage of locality:
	**Temporal locality** 
		If a program accesses data once, it’s likely to access it again
	**Spatial locality** 
		 If a program accesses some data, it’s likely to access other data that’s nearby in memory

Locality example:
```cpp
sum = 0
for (i = 0, i < n, i++){
	sum += a[i];
}
return sum
```

