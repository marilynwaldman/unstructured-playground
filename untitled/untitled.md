---
description: Reduce
---

# Reduce Abstraction

## Syntax

Reduce takes a list, a binary operation, and an identity element for the operation.  It returns a value representing the binary operator applied to successive application of the operations to intermediate results.

![Reduce](../.gitbook/assets/screen-shot-2019-01-01-at-10.04.08-am.png)

##  Example

```text
from functools import reduce
product = reduce((lambda x, y: x * y), [47, 11, 42, 13])

# Output: 113
```

