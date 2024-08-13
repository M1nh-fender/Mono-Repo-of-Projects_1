Python Nuances:
## Dictionaries
--- 
in this example code
**
magCounter = {}

for char, count in magCounter.items():
	.....
**

so char and count, the variable names for the key and value, in the dictionary items.  So calling the items() in a dictionary will return the tuples

## Heap Fundamentals
--- 
import heapq

python only have min heaps

A = [.........]
heapq.heapify(*Array*)
- Time O(n)
- Space O(1)
heapq.heappush(*Array*, *value*)
- Time O(log n)
heap.heappop(*Array*)
- O(log n)
---
Sort but own implmentation....
def heapsort(arr):
 - heapq.heapify(*Array*)
 - n = len(arry)
 - new_list = [0] * n

- for i in range(n):
	- minn = heapq.heappop(*array*)
	- new_list[i] = minn
- return new_list

return new_list

---
heapq.heappushpop

To make heapq from min to max heap, we just multiple all the values by negative one so it like basically a heapmax....