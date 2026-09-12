# DAY 11 — Rank, Axes & Shape

## 1. Rank

**Definition:**  
Rank tells us the **number of dimensions/axes** a tensor has.

```text
Scalar  → Rank 0
Vector  → Rank 1
Matrix  → Rank 2
3D      → Rank 3
4D      → Rank 4
5D      → Rank 5
```

---

# 2. Axes

**Definition:**  
Axes are the **individual dimensions/directions** along which tensor data is organized.

For a 2D matrix:

```text
[1 2 3]
[4 5 6]
```

There are two axes:

```text
Axis 0 → Rows
Axis 1 → Columns
```

Remember:

**Rank = number of axes**

---

# 3. Shape

**Definition:**  
Shape tells us **how many elements exist along each axis** of a tensor.

Example:

```text
[1 2 3]
[4 5 6]
```

There are:

```text
2 rows
3 columns
```

Therefore:

```text
Shape = (2,3)
```
