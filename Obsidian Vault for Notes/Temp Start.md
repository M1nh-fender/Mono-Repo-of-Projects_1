LeetCode Notes
- Decision Trees
- python sort on key lambda. example trucksize problem
- Bit manipulation?

Here's how you can write each of these logical operations in Python:

1. **AND**
   - Python Syntax: `and`
   - Example:
     ```python
     A = True
     B = False
     result = A and B  # Only true if both are true
     ```

2. **OR**
   - Python Syntax: `or`
   - Example:
     ```python
     A = True
     B = False
     result = A or B  # True if at least one is true
     ```

3. **NOT**
   - Python Syntax: `not`
   - Example:
     ```python
     A = True
     result = not A  # Reverses the value (True becomes False)
     ```

4. **XOR (exclusive OR)**
   - Python Syntax: `^` (bitwise XOR)
   - Example:
     ```python
     A = True
     B = False
     result = A ^ B  # True if one is true, but not both
     ```

5. **NAND (Not AND)**
   - Python Syntax: `not (A and B)`
   - Example:
     ```python
     A = True
     B = False
     result = not (A and B)  # True unless both are true
     ```

6. **NOR (Not OR)**
   - Python Syntax: `not (A or B)`
   - Example:
     ```python
     A = True
     B = False
     result = not (A or B)  # True if both are false
     ```

7. **XNOR (exclusive NOR)**
   - Python Syntax: `not (A ^ B)`
   - Example:
     ```python
     A = True
     B = False
     result = not (A ^ B)  # True if both are the same (either both True or both False)
     ```

