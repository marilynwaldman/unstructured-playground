---
description: Filter
---

# Filter Abstraction

## Syntax

Filter takes a list, list and a predicate.  It returns a list for which the predicate is true.

```text
filter(lambda x : predicate(x), list))
```

## Example

```text
num_list = range(-5, 5)
filtered_list = list(filter(lambda x: x < 0, num_list))
print(filtered_list)

# Output: [-5, -4, -3, -2, -1]
```

