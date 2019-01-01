---
description: Map
---

# Map Abstraction

## Syntax

Map applies a function, f, to all element of a list, list.

```text
map(f, list)
```

## Example

```text
items = [1, 2, 3, 4, 5]
squared = list(map(lambda x: x**2, items))
#output [2, 4,  6, 8, 10]
```

