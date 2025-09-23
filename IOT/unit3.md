Alright! Let’s break this down **clearly, point by point**, so it’s easy to understand for exams, and I’ll include **real-world examples and keywords**.

---

# **NumPy Basics**

### **1. What is NumPy?**

* **NumPy** stands for **Numerical Python**.
* It is a **Python library** used for **high-performance numerical computing**.
* At its core, NumPy uses **ndarray objects**, which are **n-dimensional arrays** that can store **homogeneous data types** (all elements of the same type).

**Example:**

```python
import numpy as np
A = np.array([1, 2, 3, 4, 5])
```

Here:

* `np.array()` creates an ndarray object.
* `A` is now a **1D array** of integers.

---

### **2. np.ndarray vs np.array**

* **`np.ndarray`**: This is a **class** in NumPy. You can create arrays using this class directly, but it is **rarely used directly**.
* **`np.array()`**: This is a **convenient method** to create an ndarray object. **Most people use this.**

**Example:**

```python
B = np.ndarray(shape=(2,3), dtype=int)
```

This creates a **2x3 array**, but usually we prefer `np.array([[1,2,3],[4,5,6]])` because it’s simpler.

---

### **3. n-dimensional Arrays**

* An **ndarray** can have **1D, 2D, or higher dimensions**.
* NumPy is designed to handle large amounts of data efficiently using **compiled C code** internally, making it **much faster than standard Python lists**.

**Example:**

```python
C = np.array([[1,2,3],[4,5,6]])  # 2D array
```

---

### **4. Differences from Standard Python Sequences**

1. **Fixed Size**:

   * Once an ndarray is created, its **size is fixed**.
   * If you want to change size, a **new array is created**.

```python
D = np.array([1,2,3])
D = np.append(D, 4)  # Creates a new array [1,2,3,4]
```

2. **Homogeneous Data**:

   * All elements in a NumPy array **must have the same data type**.
   * This allows **efficient memory storage and operations**.

```python
E = np.array([1, 2, 3], dtype=float)  # all floats
```

3. **Exception: Object Arrays**:

   * Arrays of `dtype=object` can store elements of **different sizes or types**.

```python
F = np.array([[1,2,3],[4,5]], dtype=object)
```

Here:

* The first element is a list of 3 elements, second is a list of 2 elements.
* This is **slower** than normal homogeneous arrays, but flexible.

---

### **5. Why NumPy is Fast**

* NumPy is **implemented in C**, so operations like **addition, multiplication, dot product** are **performed in compiled code**, not Python loops.
* This makes **large-scale computations extremely fast**, ideal for **data analysis, machine learning, and scientific computing**.

**Real-world example:**

* If you have 1 million sensor readings and want to compute the average:

```python
import numpy as np
data = np.random.rand(1000000)  # 1 million random numbers
mean = np.mean(data)             # very fast
```

* Doing this with a Python list would be **much slower**.

---

### **6. Keywords to Remember**

* `ndarray` → core data structure
* `np.array()` → method to create ndarray
* **Homogeneous data** → all elements same type
* **Fixed size** → cannot resize directly
* `dtype=object` → array can have different element sizes
* **Fast operations** → due to compiled C backend

---

If you want, I can **now create exam-style questions from this topic**, including **real-world scenarios**, so you can practice like your CIE 1 exam.

Do you want me to do that next?

Python List has references to objects in

Non-contiguous memory

ndarray of NumPy each element is
stored in contiguous memory space

Perfect 👍 let’s break this down clearly.

---

## 🔹 What is Vectorization in NumPy?

Vectorization means **replacing slow Python loops with fast low-level operations (C code + CPU instructions)** that process **entire arrays at once**.

---

### 🔹 Why It’s Fast?

1. **No Python loops** → loops are shifted to **C code**, which is much faster.
2. **SIMD (Single Instruction, Multiple Data)** → CPU executes one instruction on **multiple data points in parallel**.

   * Example: add 1000 numbers in one go instead of looping 1000 times.
3. **Efficient memory use** → contiguous memory in NumPy helps the CPU vectorize better.

---

### 🔹 Example

Without vectorization (Python loop):

```python
import numpy as np

a = np.array([1, 2, 3, 4])
b = np.array([5, 6, 7, 8])

c = []
for i in range(len(a)):
    c.append(a[i] + b[i])   # element-wise addition
print(c)   # [6, 8, 10, 12]
```

With vectorization (NumPy does it in C internally):

```python
c = a + b
print(c)   # [ 6  8 10 12 ]
```

👉 Here, NumPy calls optimized C code and uses **SSE instructions** to add arrays **in parallel**.

---

### 🔹 Benefits of Vectorization

* 🚀 **Speed**: Much faster than loops.
* 🔄 **Simplicity**: Code looks cleaner.
* ⚡ **Parallelism**: CPU works on many data points at once.

---

### 🔹 4–5 Mark Exam-Style Answer

**Vectorization in NumPy means executing array operations without explicit Python loops. Instead, NumPy uses optimized C code and CPU’s SIMD (SSE) instructions to process multiple elements in parallel. This improves speed, reduces complexity of code, and makes NumPy much more efficient compared to pure Python.**

---

Do you want me to also prepare a **diagram/illustration** (like "loop vs vectorized execution") for this so it’s easier to remember in exams?



