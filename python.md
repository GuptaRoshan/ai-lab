- [Python Cheatsheet](https://www.pythoncheatsheet.org/cheatsheet/dictionaries)

### The Standard Entry Point

```python
if __name__ == "__main__":
    main()
```

This allows the file to be:

- **Run directly** → executes `main()`.
- **Imported as a module** → does **not** execute `main()`.

### 👇 Example:

```python
def main():
    print("This is the main function.")

print("Top-level code runs.")

if __name__ == "__main__":
    main()
```

### Output when run directly:

```
Top-level code runs.
This is the main function.
```

### Output when imported into another script:

```
Top-level code runs.
```

(Note: `main()` does **not** run unless called)

### For Loop


**1. Simple Loop**

```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)
```


**2. Loop with Index using `range()`**

```python
fruits = ["apple", "banana", "cherry"]

for i in range(len(fruits)):
    print(i, fruits[i])
```


**3. Using `enumerate()` for Index + Value**

```python
fruits = ["apple", "banana", "cherry"]

for index, fruit in enumerate(fruits):
    print(f"Index {index}: {fruit}")
```


### While Loop

```python
# Print numbers from 1 to 5 using a while loop

count = 1
while count <= 5:
    print("Count is:", count)
    count += 1
```

### Conditions



### 🧮 1. **Bitwise Operators**

| Operator | Name        | Example    | Result |     |     |
| -------- | ----------- | ---------- | ------ | --- | --- |
| `&`      | Bitwise AND | `5 & 3`    | `1`    |     |     |
| \`       | \`          | Bitwise OR | \`5    | 3\` | `7` |
| `^`      | Bitwise XOR | `5 ^ 3`    | `6`    |     |     |
| `~`      | Bitwise NOT | `~5`       | `-6`   |     |     |
| `<<`     | Left Shift  | `5 << 1`   | `10`   |     |     |
| `>>`     | Right Shift | `5 >> 1`   | `2`    |     |     |


### ⚖️ 2. **Comparison Operators**

| Operator | Name                  | Example  | Result |
| -------- | --------------------- | -------- | ------ |
| `==`     | Equal to              | `5 == 5` | `True` |
| `!=`     | Not equal to          | `5 != 3` | `True` |
| `>`      | Greater than          | `5 > 3`  | `True` |
| `<`      | Less than             | `3 < 5`  | `True` |
| `>=`     | Greater than or equal | `5 >= 5` | `True` |
| `<=`     | Less than or equal    | `4 <= 5` | `True` |

### 🔘 3. **Boolean (Logical) Operators**

| Operator | Name        | Example          | Result  |
| -------- | ----------- | ---------------- | ------- |
| `and`    | Logical AND | `True and False` | `False` |
| `or`     | Logical OR  | `True or False`  | `True`  |
| `not`    | Logical NOT | `not True`       | `False` |


### lambda

#### **Syntax of lambda**

```python
lambda arguments: expression
```

- `lambda` is the keyword.
- `arguments` are the input parameters.
- `expression` is a single expression executed and returned.

#### ✅ **Basic Example**

```python
add = lambda x, y: x + y
print(add(2, 3))  # Output: 5
```

This is equivalent to:

```python
def add(x, y):
    return x + y
```

#### ✅ **Lambda with `map()`**

```python
nums = [1, 2, 3, 4]
squares = list(map(lambda x: x**2, nums))
print(squares)  # Output: [1, 4, 9, 16]
```

#### ✅ **Lambda with `filter()`**

```python
nums = [1, 2, 3, 4, 5, 6]
even_nums = list(filter(lambda x: x % 2 == 0, nums))
print(even_nums)  # Output: [2, 4, 6]
```

#### ✅ **Lambda with `sorted()`**

```python
points = [(2, 3), (1, 9), (4, 1)]
sorted_points = sorted(points, key=lambda point: point[1])
print(sorted_points)  # Output: [(4, 1), (2, 3), (1, 9)]
```

#### ✅ **Lambda Inside Function Calls**

```python
def apply_operation(x, func):
    return func(x)

result = apply_operation(5, lambda x: x * x)
print(result)  # Output: 25
```

### Lists and Tuples

### Dictionaries

### Sets

### Comprehensions

### Strings

### Args and Kwargs

### Built-in Data Structures

| Type          | Description                             | Mutable? | Ordered? | Key Features                               | Example Code                                                                              |
|---------------|-----------------------------------------|----------|----------|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `list`        | Ordered, resizable array                | ✅        | ✅        | Indexing, slicing, duplicates allowed      | `lst = [1, 2, 3]; lst.append(4)`                                                          |
| `tuple`       | Ordered, immutable list                 | ❌        | ✅        | Faster, hashable if all items are hashable | `tpl = (1, 2, 3); print(tpl[0])`                                                          |
| `set`         | Unordered, unique items                 | ✅        | ❌        | No duplicates, fast membership checks      | `s = {1, 2}; s.add(3)`                                                                    |
| `frozenset`   | Immutable set                           | ❌        | ❌        | Hashable, can be dict keys                 | `fs = frozenset([1, 2, 3])`                                                               |
| `dict`        | Key-value pairs (map in Java)           | ✅        | ✅\*      | Fast lookups, keys are unique              | `d = {'a': 1}; d['b'] = 2`                                                                |
| `str`         | Immutable text sequence                 | ❌        | ✅        | Unicode support, slicing, formatting       | `s = "hello"; print(s.upper())`                                                           |
| `bytearray`   | Mutable array of bytes                  | ✅        | ✅        | Useful for binary data                     | `ba = bytearray(b'abc'); ba[0] = 65`                                                      |
| `bytes`       | Immutable array of bytes                | ❌        | ✅        | Supports encoding, decoding                | `b = b'hello'; print(b[0])`                                                               |
| `deque`       | Double-ended queue (from `collections`) | ✅        | ✅        | Fast appends/pops on both ends             | `from collections import deque; dq = deque([1]); dq.appendleft(0)`                        |
| `Counter`     | Multiset (from `collections`)           | ✅        | ❌        | Counts of hashable objects                 | `from collections import Counter; c = Counter("banana")`                                  |
| `defaultdict` | Dict with default values                | ✅        | ✅\*      | Avoids key errors                          | `from collections import defaultdict; dd = defaultdict(int); dd['a'] += 1`                |
| `OrderedDict` | Dict that remembers insert order        | ✅        | ✅        | (Preserved in 3.7+ by default)             | `from collections import OrderedDict; od = OrderedDict(); od['a'] = 1`                    |
| `NamedTuple`  | Tuple with named fields                 | ❌        | ✅        | Readable, structured records               | `from collections import namedtuple; Point = namedtuple('Point', 'x y'); p = Point(1, 2)` |
| `heapq`       | Heap queue (priority queue)             | ✅        | ❌        | Min-heap operations                        | `import heapq; h = [3, 1, 2]; heapq.heapify(h); heapq.heappop(h)`                         |
