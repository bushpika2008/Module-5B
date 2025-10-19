# NumPy Program: Column-wise Sorting of a 2D Array

## 🎯 Aim
To write a **NumPy** program that sorts the elements in each column of a given 2D array in ascending order.

## 🧠 Algorithm

1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Accept a 2D NumPy array from the user.
3. **Sort Column-wise**: Use the `np.sort()` function with `axis=0` to sort each column in ascending order.
4. **Store Result**: Store the sorted result in a new array.
5. **Display Output**: Print the original array and the column-wise sorted array.

## 🧾 Program
Add code here
```
import numpy as np

# Accept input for 2D array
rows = int(input("Enter number of rows: "))
cols = int(input("Enter number of columns: "))

print("Enter the elements row-wise (space-separated):")
arr = []
for i in range(rows):
    arr.append(list(map(int, input().split())))

# Convert to NumPy array
array = np.array(arr)

# Column-wise sorting
sorted_array = np.sort(array, axis=0)

# Display results
print("\nOriginal Array:")
print(array)

print("\nColumn-wise Sorted Array:")
print(sorted_array)

```


## Output
<img width="556" height="324" alt="image" src="https://github.com/user-attachments/assets/71b611b1-9f43-4f95-b3ab-ef25d76c19a5" />



## Result
The program successfully accepts a 2D array from the user, sorts each column in ascending order, and prints both the original and column-wise sorted arrays using NumPy.

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

``# 🧪 Pandas Program: Join Two DataFrames Along Rows

## 🎯 AIM

To write a Python program using Pandas to **join two DataFrames along rows** (row-wise concatenation) and assign all data to a new DataFrame.

---

## 🧠 ALGORITHM

1. **Import Libraries**: Import the `pandas` library.
2. **Create First DataFrame**: Use a dictionary to create `student_data1`.
3. **Create Second DataFrame**: Use another dictionary to create `student_data2`.
4. **Concatenate DataFrames**: Use `pd.concat()` with `axis=0` to concatenate both DataFrames row-wise.
5. **Display Result**: Print the new combined DataFrame.

---

## 💻 Program
```
import pandas as pd
df1 = pd.DataFrame({
    'A': [1, 2, 3],
    'B': ['a', 'b', 'c']
})
df2 = pd.DataFrame({
    'A': [4, 5, 6],
    'B': ['d', 'e', 'f']
})
df_new = pd.concat([df1, df2], axis=0, ignore_index=True)
print("New DataFrame after row-wise concatenation:")
print(df_new)
```

## Output

![WhatsApp Image 2025-10-14 at 22 12 39_dc886e44](https://github.com/user-attachments/assets/c3aee9ee-b7e3-4484-95ac-5b2576bb7f90)


## Result
The program successfully **join two DataFrames along rows** (row-wise concatenation) and assign all data to a new DataFrame.

# Pandas Program: Create and Display a DataFrame with Custom Index Labels

## 🎯 Aim

To create and display a **DataFrame** using the **Pandas** library in Python from a given dictionary, and apply specific index labels to the rows.

---

## 🧠 Algorithm

1. **Import Libraries**: Import the required libraries – `pandas` and `numpy`.
2. **Create Dictionary**: Define a dictionary `exam_data` with keys: `'name'`, `'score'`, `'attempts'`, and `'qualify'`.
3. **Index Labels**: Create a list of custom index labels called `labels`.
4. **Create DataFrame**: Use `pd.DataFrame()` to create the DataFrame by passing the dictionary and index labels.
5. **Display Output**: Display the DataFrame using `print()` or by simply calling the DataFrame variable.

---

## 💻 Program
Add code here
```
import pandas as pd
import numpy as np

# Create dictionary with exam data
exam_data = {
    'name': ['Alice', 'Bob', 'Charlie', 'David', 'Eva'],
    'score': [85, 92, 78, 90, 88],
    'attempts': [1, 3, 2, 1, 2],
    'qualify': ['yes', 'yes', 'no', 'yes', 'yes']
}

# Custom index labels
labels = ['a', 'b', 'c', 'd', 'e']

# Create DataFrame with custom index
df = pd.DataFrame(exam_data, index=labels)

# Display the DataFrame
print(df)

```

## Output
<img width="720" height="580" alt="image" src="https://github.com/user-attachments/assets/0092176c-97bb-45ea-8e64-de995da731c0" />


## Result
The program successfully creates a Pandas DataFrame from a dictionary and applies custom index labels.
The DataFrame displays all columns (name, score, attempts, qualify) along with the specified row indices (a, b, c, d, e).
