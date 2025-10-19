# # NumPy Program: Find Indices Where Elements in Array x are Greater Than or Equal to Corresponding Elements in Array y

## 🎯 Aim
To write a Python program using **NumPy** that finds the indices where elements in array `x` are greater than or equal to their corresponding elements in array `y`.

## 🧠 Algorithm
1. **Import NumPy**: Import the NumPy library.
2. **Define Arrays**: Define two NumPy arrays, `x` and `y`, with the same shape (i.e., same number of elements).
3. **Use Boolean Indexing**: 
   - `x > y` gives a boolean array where elements of `x` are greater than `y`.
   - `x == y` gives a boolean array where elements of `x` are equal to `y`.
4. **Find Indices**: Use `np.where()` to get the indices where the conditions `x >= y` are satisfied.
5. **Print Indices**: Print the indices where the condition holds true.

## 🧾 Program
```
import numpy as np
x = np.array([5, 3, 7, 1, 9])
y = np.array([2, 4, 7, 0, 10])
indices = np.where(x >= y)[0]

print("Indices where x >= y:", indices)
```

## Output
![WhatsApp Image 2025-10-14 at 22 09 22_df0ad824](https://github.com/user-attachments/assets/4a48342b-3d43-4f40-98bb-4519fabdad8a)

## Result
The program successfully  finds the indices where elements in array `x` are greater than or equal to their corresponding elements in array `y`.
