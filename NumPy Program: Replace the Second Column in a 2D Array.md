# NumPy Program: Replace the Second Column in a 2D Array

## 🎯 Aim
To write a **NumPy** program that deletes the second column from a given 2D array and inserts a new column at the same position.

## 🧠 Algorithm
1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Get a 2D NumPy array and a new column (as another array) from the user.
3. **Delete Column**: Use `np.delete()` to remove the second column (index 1) from the original array.
4. **Insert Column**: Use `np.insert()` to insert the new column at the second column's original position.
5. **Display Result**: Print the updated array with the replaced column.

## 🧾 Program
```
import numpy as np

# Define the original 2D array
arr = np.array([[1, 2, 3],
                [4, 5, 6],
                [7, 8, 9]])

# Delete the second column (index 1)
arr_deleted = np.delete(arr, 1, axis=1)

# Define the new column to insert
new_col = np.array([10, 11, 12])

# Insert the new column at the same position (index 1)
arr_modified = np.insert(arr_deleted, 1, new_col, axis=1)

print("Original array:\n", arr)
print("Array after deleting second column:\n", arr_deleted)
print("Array after inserting new column:\n", arr_modified)
```


## Output
![WhatsApp Image 2025-10-14 at 22 03 59_5433ce25](https://github.com/user-attachments/assets/91fcc2be-650e-4e73-88d4-be77657d376e)

## Result
The program successfully deletes the second column from 2D array using numpy
