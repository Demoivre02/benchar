# Benchar - String Comparison Counter

The `benchar` class is a Python utility for counting string comparison operations during string manipulations. It extends the behavior of the built-in `str` class to keep track of the count of character comparisons performed using methods like `__eq__`, `__ne__`, `__lt__`, `__le__`, `__gt__`, `__ge__`, `endswith`, and `startswith`.

## Usage

To use `benchar`, follow the steps below:

### Initialization

```python
from benchar import benchar

# Create an instance of benchar
counter = benchar()
```

### String Operations

Any string created from an instance of `benchar` will keep track of comparison operations.

```python
# Example string operations
string1 = counter("hello")
string2 = counter("hella")

# Perform string comparisons
result = string1 == string2

# Access comparison count
comparison_count = counter.cmp_count
print(f"String Comparison Count: {comparison_count}")
```

### Supported Operations

- `__eq__`: Equal to
- `__ne__`: Not equal to
- `__lt__`: Less than
- `__le__`: Less than or equal to
- `__gt__`: Greater than
- `__ge__`: Greater than or equal to
- `endswith`: Checks if the string ends with a specified suffix
- `startswith`: Checks if the string starts with a specified prefix

### Note

The comparison count is incremented based on the index of the first differing character during comparisons.

## Example

```python
# Example usage of benchar
counter_instance = benchar()

# Create strings and perform operations
string1 = counter_instance("apple")
string2 = counter_instance("aple")
result = string1 == string2

# Access and print the comparison count
comparison_count_result = counter_instance.cmp_count
print(f"String Comparison Count: {comparison_count_result}")
```

## Note

Ensure that you have the `benchar` module available in your project. This utility is useful for tracking the number of character comparisons during string manipulations and can be integrated into projects where detailed comparison statistics are required.