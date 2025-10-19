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
