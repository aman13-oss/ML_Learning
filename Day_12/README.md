# DAY 12 — 3D, 4D & 5D Tensors

## 1. 3D Tensor

**Definition:**  
A 3D tensor contains data organized along **three axes**.

Example:

```text
[
  [
    [1,2],
    [3,4]
  ],

  [
    [5,6],
    [7,8]
  ]
]
```

Shape:

```text
(2,2,2)
```

Rank:

```text
3
```

### Real-world example

A grayscale image dataset can be represented as:

```text
(number of images, height, width)
```

---

# 2. 4D Tensor

A common example is a **batch of images**.

Shape:

```text
(batch, height, width, channels)
```

Example:

```text
(10, 64, 64, 3)
```

Meaning:

```text
10       → Images
64       → Height
64       → Width
3        → Color channels
```

Rank:

```text
4
```

---

# 3. 5D Tensor

A common example is a **batch of videos**.

Shape:

```text
(batch, frames, height, width, channels)
```

Example:

```text
(8, 20, 64, 64, 3)
```

Meaning:

```text
8   → Videos
20  → Frames per video
64  → Height
64  → Width
3   → Color channels
```

Rank:

```text
5
```
