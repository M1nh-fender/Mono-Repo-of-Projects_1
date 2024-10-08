Purpose: To understand the python nuances

*Template*
```python

     ```
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

## Python List Comprehension
---
- [expression for item in iterable if condition]
     ```python
	squares = [x**2 for x in range(10)]
	or
	evens = [x for x in range(10) if x % 2 == 0]
	or
	uppercase_words = [words.upper() for word in words]
     ```

### **Harder example**
```python
flat_list = [item for sublist in matrix for item in sublist]
```

### Equivalent Expanded For Loops:
```python
# Initialize an empty list to store the flattened elements
flat_list = []

# Outer loop to iterate over each sublist in the matrix
for sublist in matrix:
    # Inner loop to iterate over each item in the current sublist
    for item in sublist:
        # Append the item to the flat_list
        flat_list.append(item)

# The flat_list now contains all the elements from the sublists
print(flat_list)
```

### Breakdown of the Explicit For Loops:
1. **`flat_list = []`**:
   - We start by initializing an empty list where the flattened values will be stored.
   
2. **Outer Loop**:
   ```python
   for sublist in matrix:
   ```
   - This outer loop iterates over each inner list (or sublist) inside `matrix`.
   - For example, in the first iteration, `sublist` is `[1, 2, 3]`.
   - In the second iteration, `sublist` is `[4, 5, 6]`, and so on.

3. **Inner Loop**:
   ```python
   for item in sublist:
   ```
   - Inside the outer loop, this inner loop iterates over each element (or item) in the current `sublist`.
   - For example, if `sublist` is `[1, 2, 3]`, the inner loop will go over `1`, `2`, and `3`.

4. **Append to List**:
   ```python
   flat_list.append(item)
   ```
   - During each iteration of the inner loop, the current `item` is appended to `flat_list`.

### Visual Execution of Loops:
Here’s what happens step by step:

1. **First iteration of the outer loop**:
   - `sublist = [1, 2, 3]`
   - The inner loop runs:
     - `item = 1` → `flat_list = [1]`
     - `item = 2` → `flat_list = [1, 2]`
     - `item = 3` → `flat_list = [1, 2, 3]`

2. **Second iteration of the outer loop**:
   - `sublist = [4, 5, 6]`
   - The inner loop runs:
     - `item = 4` → `flat_list = [1, 2, 3, 4]`
     - `item = 5` → `flat_list = [1, 2, 3, 4, 5]`
     - `item = 6` → `flat_list = [1, 2, 3, 4, 5, 6]`

3. **Third iteration of the outer loop**:
   - `sublist = [7, 8, 9]`
   - The inner loop runs:
     - `item = 7` → `flat_list = [1, 2, 3, 4, 5, 6, 7]`
     - `item = 8` → `flat_list = [1, 2, 3, 4, 5, 6, 7, 8]`
     - `item = 9` → `flat_list = [1, 2, 3, 4, 5, 6, 7, 8, 9]`

### Final Result:
At the end, `flat_list` contains all the items from the matrix in one flat list:
```python
flat_list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

## Bit Manipulation
---
### 1. **AND**
   - Python Syntax: `and`
   - Example:
     ```python
     A = True
     B = False
     result = A and B  # Only true if both are true
     ```

 ### 2. **OR**
   - Python Syntax: `or`
   - Example:
     ```python
     A = True
     B = False
     result = A or B  # True if at least one is true
     ```

### 3. **NOT**
   - Python Syntax: `not`
   - Example:
     ```python
     A = True
     result = not A  # Reverses the value (True becomes False)
     ```

### 4. **XOR (exclusive OR)**
   - Python Syntax: `^` (bitwise XOR)
   - Example:
     ```python
     A = True
     B = False
     result = A ^ B  # True if one is true, but not both
     ```

### 5. **NAND (Not AND)**
   - Python Syntax: `not (A and B)`
   - Example:
     ```python
     A = True
     B = False
     result = not (A and B)  # True unless both are true
     ```

### 6. **NOR (Not OR)**
   - Python Syntax: `not (A or B)`
   - Example:
     ```python
     A = True
     B = False
     result = not (A or B)  # True if both are false
     ```

### 7. **XNOR (exclusive NOR)**
   - Python Syntax: `not (A ^ B)`
   - Example:
     ```python
     A = True
     B = False
     result = not (A ^ B)  # True if both are the same (either both True or both False)
     ```


## Basic Operation
---
// is floor division, so number rounded down

## Graphs
---
Link to online notes of Python graphs: [Graphs - Data Structures & Algorithms Course - Colab (google.com)](https://colab.research.google.com/drive/1V5Afu8zDQLJpPXQLMyocMm93GB2qdOJV)
### Edge Lists
```python
numberOfEdges = 8
	
ArrayOfEdges = [[0, 1], [1, 2], [0, 3], [3, 4], [3, 6], [3, 7], [4, 2], [4, 5], [5, 2]]
     ```
- Here, this can be interepted as a directed graph.  There is an edge from node 0 to 1, 1 to 2 .... 3 to 4, 3 to 6, 3 to 7
### Array of Edges -> Adjacency Matrix
```python
M = []
for i in range(numberOfRows):
	M.append([0] * numberOfColumns) #so in each row, we add the number of columns

for startVertex, endingVertex in ArrayOfEdges:
	M[startVertex][endingVertex] = 1

	M[endingVertex][startVertex] = 1 #if graph is undirected
     ```

### Array of Edges -> Adjacency List
```python
from collections import defaultdict

D = defaultdict(list)

for u, v in ArrayOfEdges:
  D[u].append(v)

  # Uncomment the following line if the graph is undirected
  # D[v].append(u)
print(A)
Output => defaultdict(list, {0: [1, 3], 1: [2], 3: [4, 6, 7], 4: [2, 5], 5: [2]})

print(D[3])
Output => [4, 6, 7] #Node 3 connects to node 4, 6, 7

print(M[3])
Output => [0, 0, 0, 0, 1, 0, 1, 1] #Same thing as before but not as clear
				#Nodes 4     6  7
```

### DFS
---
- Recursive
```python
D = defaultdict(list) #from above... ^

def dfs_recursive(node):
	print(node) #Processing
	for neighborN in D[node]:
		if neighborN not in seen:
			seen.add
			dfs_recursive(neighborN)

source = 0
seen = set()
see.add(source)
dfs_recursive(source)
     ```

- Iterative
```python
source = 0

seen = set()
seen.add(source)
stack = [source]

while stack:
	node = stack.pop()
	print(node)
	for neighborN in D[node]:
		if neighborN not in seen:
			seen.add(neighborN)
			stack.append(neighborN)

     ```

### BFS
---
```python
source = 0

from collections import deque

seen = set()
see.add(source)
q = deque()
q.append(source)

while q:
	node = q.popleft()
	print(node)
	for neighborN in D[node]:
		if neighborN not in seen:
			seen.add(neighborN)
			q.append(neighborN)

     ```


## String manipulation shananigans....
---
### .isalnum()
```python
s[x].isalnum()
     ```
### import re (regular expression)

```python
	import re
    cleaned_string = re.sub(r'[^a-zA-Z0-9]', '', input_string)
```


- `re.sub(pattern, replacement, string, count=0, flags=0)`
- It replaces occurrences of the `pattern` in the `string` with the specified `replacement`.
- You can control the number of replacements using the optional `count` parameter.

```python
import re

txt = "The rain in Spain"
result = re.sub("s", "9", txt)
print(result)  # Output: "The rain in 9pain"
```

- There is a flag option as well
```python
import re
txt = "Apples are tasty."
result = re.sub(r"apple", "banana", txt, flags=re.IGNORECASE)
print(result)  # Output: "bananas are tasty."
```

---
# Recursion Note
---
```python
class Solution(object):

    def diameterOfBinaryTree(self, root):
        """
        :type root: TreeNode
        :rtype: int
        """
        largestDiameter = [0] #**Why do we have this?**

        def height(treeNode):
            if treeNode is None:
                return 0

            leftHeight = height(treeNode.left)
            rightHeight = height(treeNode.right)
            diameter = leftHeight + rightHeight

            largestDiameter[0] = max(largestDiameter[0], diameter)
            
            return 1 + max(leftHeight, rightHeight)

        height(root)
        return largestDiameter[0]
     ```
- The reason we have *largestDiameter = [0]* is because in the recursive call, if we did not have an array and had like *largestDiameter  = 0*, largestDiameter would be a local variable in that call of the recursion and we need a global variable to be updated.  So having it an array element would make it global


# Enumeration
---
```python
# A list of items
fruits = ['apple', 'banana', 'cherry']


for index, varName in enumerate(*array*):
    print(index, varName)

# Using enumerate to loop over the list with an index
for index, fruit in enumerate(fruits):
    print(index, fruit)


Note, index is always first then the variable name of the item

Output below
--------------
0 apple
1 banana
2 cherry

     ```

# any() --- The any function
---
Copy paste from online...
In Python, both `any()` and `map()` functions are used for different purposes:

### `any()` Function
- **Purpose**: Checks if any element in an iterable is `True`.
- **Return Value**: Returns `True` if at least one element in the iterable is `True`. Otherwise, it returns `False`.
- **Usage**: Commonly used when you want to check if there's at least one `True` value in a list, tuple, or other iterable.

**Example**:
```python
# List of values
values = [0, 0, 1, 0]

# Check if any value is True (non-zero in this case)
result = any(values)

print(result)  # Output: True
```

### `map()` Function
- **Purpose**: Applies a specified function to every item of an iterable (like a list or tuple) and returns a map object (which is an iterator).
- **Return Value**: Returns a map object, which can be converted into a list, tuple, etc., to see the results.
- **Usage**: Useful when you want to apply a function to each item in an iterable.

**Example**:
```python
# Function to double a number
def double(x):
    return x * 2

# List of values
values = [1, 2, 3, 4]

# Apply the double function to each element in the list
result = map(double, values)

# Convert the map object to a list and print it
print(list(result))  # Output: [2, 4, 6, 8]


```

### Key Differences
- **Functionality**: `any()` is for checking conditions across an iterable, while `map()` is for transforming each element in an iterable.
- **Return Type**: `any()` returns a single boolean value, whereas `map()` returns an iterator of transformed elements.
- **Use Case**: Use `any()` when you need to check if there's any `True` value, and `map()` when you want to apply a function to all elements in an iterable.



# Binary Search with a condition
---
Before I usually think of finding a target but binary search can also be used to find first occurring condition

```python
# Condition based
B = [False, False, False, False, False, False, True]

def binary_search_condition(arr):
  N = len(arr)
  L = 0
  R = N - 1

  while L < R:
    M = (L + R) // 2

    if B[M]:
      R = M
    else:
      L = M + 1
  return L

binary_search_condition(B)

(prints out 6)
```


# Nonlocal
---
```python

     ```
Used to use variables outside of the scope of a function:
[Python nonlocal Keyword - GeeksforGeeks](https://www.geeksforgeeks.org/python-nonlocal-keyword/)

Not used for global variables....
# ZIP
---
```python
name = [ "Manjeet", "Nikhil", "Shambhavi", "Astha" ]
roll_no = [ 4, 1, 3, 2 ]

# using zip() to map values
mapped = zip(name, roll_no)

print(set(mapped))
     ```
 output: {('Nikhil', 1), ('Shambhavi', 3), ('Manjeet', 4), ('Astha', 2)}

In this example, zip will map each array to have each index correspond with one another

## Dictionary application as well
```python
stocks = ['GEEKS', 'For', 'geeks']
prices = [2175, 1127, 2750]

new_dict = {stocks: prices for stocks,
            prices in zip(stocks, prices)}
print(new_dict)

     ```
output: {'GEEKS': 2175, 'For': 1127, 'geeks': 2750}