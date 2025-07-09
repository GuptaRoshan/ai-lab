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

#### **Basic Example**

```python
add = lambda x, y: x + y
print(add(2, 3))  # Output: 5
```

This is equivalent to:

```python
def add(x, y):
    return x + y
```

#### **Lambda with `map()`**

```python
nums = [1, 2, 3, 4]
squares = list(map(lambda x: x**2, nums))
print(squares)  # Output: [1, 4, 9, 16]
```

#### **Lambda with `filter()`**

```python
nums = [1, 2, 3, 4, 5, 6]
even_nums = list(filter(lambda x: x % 2 == 0, nums))
print(even_nums)  # Output: [2, 4, 6]
```

#### **Lambda with `sorted()`**

```python
points = [(2, 3), (1, 9), (4, 1)]
sorted_points = sorted(points, key=lambda point: point[1])
print(sorted_points)  # Output: [(4, 1), (2, 3), (1, 9)]
```

#### **Lambda Inside Function Calls**

```python
def apply_operation(x, func):
    return func(x)

result = apply_operation(5, lambda x: x * x)
print(result)  # Output: 25
```

### Lists and Tuples

#### Creation

```python
my_list = [1, 2, 3]
empty_list = list()
```

#### Accessing Items

```python
my_list[0]     # First item
my_list[-1]    # Last item
```

#### Modifying

```python
my_list[0] = 10         # Change item
my_list.append(4)       # Add at end
my_list.insert(1, 99)   # Insert at position
my_list.extend([5, 6])  # Extend with another list
```

#### Removing

```python
my_list.remove(10)      # Remove first match
del my_list[0]          # Delete by index
my_list.pop()           # Pop last item
my_list.clear()         # Empty the list
```

#### Searching

```python
my_list.index(99)       # Index of value
99 in my_list           # Check existence
my_list.count(2)        # Count occurrences
```

#### Sorting

```python
my_list.sort()          # In-place sort
sorted_list = sorted(my_list)  # New sorted list
my_list.reverse()       # Reverse in place
```

#### Slicing

```python
my_list[1:3]            # Slice from index 1 to 2
my_list[:3]             # From start to index 2
my_list[::2]            # Every 2nd element
```

#### Looping

```python
for item in my_list:
    print(item)
```

### Dictionaries


| **Category**         | **Code / Example**                                              | **Description**                      |
|----------------------|-----------------------------------------------------------------|--------------------------------------|
| **Creation**         | `my_dict = {'a': 1, 'b': 2}`<br>`dict(x=3, y=4)`                | Create a dictionary                  |
| **Accessing**        | `my_dict['a']`<br>`my_dict.get('a')`<br>`my_dict.get('x', 0)`   | Get value; safe get with default     |
| **Adding/Updating**  | `my_dict['c'] = 3`<br>`my_dict.update({'d': 4})`                | Add or update key-value pairs        |
| **Removing**         | `del my_dict['a']`<br>`my_dict.pop('b')`<br>`my_dict.popitem()` | Remove by key; pop last item         |
| **Check Existence**  | `'a' in my_dict`<br>`'z' not in my_dict`                        | Check if key exists                  |
| **Dictionary Views** | `my_dict.keys()`<br>`my_dict.values()`<br>`my_dict.items()`     | Get keys, values, items              |
| **Looping**          | `for k in my_dict:`<br>`for k, v in my_dict.items():`           | Iterate over keys or key-value pairs |
| **Comprehension**    | `{x: x**2 for x in range(3)}`                                   | Dict comprehension                   |
| **Nested Dict**      | `nested['person']['name']`                                      | Accessing values in nested dicts     |
| **Copying**          | `copy = my_dict.copy()`<br>`deepcopy = copy.deepcopy(my_dict)`  | Shallow and deep copy                |


### Sets


| **Category**          | **Code / Example**                                                                             | **Description**                          |                      |
|-----------------------|------------------------------------------------------------------------------------------------|------------------------------------------|----------------------|
| **Creation**          | `my_set = {1, 2, 3}`<br>`empty_set = set()`                                                    | Create a set; use `set()` for empty      |                      |
| **Accessing**         | *(Not indexable like lists)*                                                                   | Sets are unordered, no indexing          |                      |
| **Adding**            | `my_set.add(4)`                                                                                | Add one item                             |                      |
| **Updating**          | `my_set.update([5, 6])`                                                                        | Add multiple items                       |                      |
| **Removing**          | `my_set.remove(2)`<br>`my_set.discard(3)`                                                      | Remove item (error if not found vs safe) |                      |
| **Pop & Clear**       | `my_set.pop()`<br>`my_set.clear()`                                                             | Pop random item, remove all              |                      |
| **Membership Test**   | `2 in my_set`<br>`7 not in my_set`                                                             | Check if item exists                     |                      |
| **Set Operations**    | `a \ b  (union) ,  a & b (intersection) ,  a - b (difference) ,  a ^ b (symmetric difference)` | Combine/compare sets                     |                      |
| **Set Comparisons**   | `a == b`<br>`a.issubset(b)`<br>`a.issuperset(b)`<br>`a.isdisjoint(b)`                          | Equality and subset checks               |                      |
| **Looping**           | `for item in my_set:`                                                                          | Iterate over items                       |                      |
| **Set Comprehension** | `{x for x in range(5) if x % 2 == 0}`                                                          | Set comprehension                        |                      |
| **Conversion**        | `set([1, 2, 2, 3])`                                                                            | Remove duplicates from list              |                      |


### Comprehensions


#### Python Comprehension Cheat Sheet

| **Type**      | **Syntax**                            | **Description / Example**               |
|---------------|---------------------------------------|-----------------------------------------|
| **List**      | `[x for x in iterable]`               | Basic list comprehension                |
|               | `[x for x in range(5) if x % 2 == 0]` | With condition: `[0, 2, 4]`             |
| **Set**       | `{x for x in iterable}`               | Creates a set with unique elements      |
| **Dict**      | `{k: v for k, v in iterable}`         | Builds a dictionary from iterable pairs |
|               | `{x: x**2 for x in range(4)}`         | `{0: 0, 1: 1, 2: 4, 3: 9}`              |
| **Generator** | `(x for x in iterable)`               | Lazy-evaluated generator                |


#### With `if-else` inside comprehension

| **Example**                                              | **Explanation**                    |
|----------------------------------------------------------|------------------------------------|
| `[x if x % 2 == 0 else -x for x in range(5)]`            | Conditional expression inside list |
| `{x: 'even' if x % 2 == 0 else 'odd' for x in range(3)}` | Dict with conditional values       |


#### Nested Comprehensions

| **Example**                                     | **Creates**                                  |
|-------------------------------------------------|----------------------------------------------|
| `[[i * j for j in range(3)] for i in range(3)]` | 2D list: `[[0, 0, 0], [0, 1, 2], [0, 2, 4]]` |



### Strings

| **Category**             | **Code / Example**                                        | **Description**                                    |
|--------------------------|-----------------------------------------------------------|----------------------------------------------------|
| **Creation**             | `'hello'`, `"world"`<br>`'''multi'''`, `"""line"""`       | Define single-line and multi-line strings          |
| **Accessing**            | `s[0]`, `s[-1]`                                           | Indexing: first and last character                 |
| **Slicing**              | `s[1:4]`, `s[:3]`, `s[::2]`                               | Substring extraction                               |
| **Length**               | `len(s)`                                                  | Get length of string                               |
| **Concatenation**        | `'Hi ' + 'there'`                                         | Combine strings                                    |
| **Repetition**           | `'ha' * 3`                                                | Repeat string: `'hahaha'`                          |
| **Membership**           | `'a' in s`, `'z' not in s`                                | Check if a character/substring exists              |
| **Case Conversion**      | `s.upper()`, `s.lower()`<br>`s.title()`, `s.capitalize()` | Change string casing                               |
| **Trimming**             | `s.strip()`, `s.lstrip()`, `s.rstrip()`                   | Remove whitespace                                  |
| **Finding/Substitution** | `s.find('a')`, `s.replace('a', 'b')`                      | Search and replace substrings                      |
| **Splitting & Joining**  | `s.split(',')`, `' '.join(list)`                          | Split string into list / join list into string     |
| **Formatting**           | `f"Name: {name}"`<br>`"Age: {}".format(age)`              | f-strings and `.format()` for formatting           |
| **Escape Sequences**     | `\n` (newline), `\t` (tab), `\\` (backslash)              | Special characters                                 |
| **Immutability**         | ❌ `s[0] = 'H'`                                            | Strings are immutable — cannot be changed in-place |
| **Looping**              | `for c in s:`                                             | Iterate over characters                            |



### Args and Kwargs

#### 1. `*args` (Non-keyword Variable Arguments)

* Collects **extra positional arguments** as a **tuple**.
* Useful when you want to pass any number of positional arguments.

```python
def my_function(*args):
    for arg in args:
        print(arg)

my_function(1, 2, 3)
# Output:
# 1
# 2
# 3
```

#### 2. `**kwargs` (Keyword Variable Arguments)

* Collects **extra keyword arguments** as a **dictionary**.
* Useful when you want to handle named arguments dynamically.

```python
def my_function(**kwargs):
    for key, value in kwargs.items():
        print(f"{key} = {value}")

my_function(name="Alice", age=30)
# Output:
# name = Alice
# age = 30
```


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
