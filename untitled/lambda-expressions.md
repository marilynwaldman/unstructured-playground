---
description: Syntax and Examples
---

# Lambda Expressions

## Syntax

```text
lambda x1,x2, ... ,xn: function( x1 x2 ... xn)
     for n >= 1
```

## Examples

### Add

```text
add = lambda x, y: x + y

print(add(3, 5))
# Output: 8
```

### Sorting a list of 2-tuples

```text
a = [(1, 2), (4, 1), (9, 10), (13, -3)]
a.sort(key=lambda x: x[1])

print(a)
# Output: [(13, -3), (4, 1), (1, 2), (9, 10)]
```

