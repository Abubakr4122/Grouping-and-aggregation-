# Grouping-and-aggregation-
  24-03-25
16. Grouping and aggregation 
import pandas as pd
data = {
    'Department': ['HR', 'IT', 'HR', 'Finance', 'IT', 'Finance', 'HR', 'IT'],
    'Employee': ['Alice', 'Bob', 'Charlie', 'David', 'Eve', 'Frank', 'Grace', 'Hank'],
    'Salary': [50000, 70000, 60000, 80000, 75000, 90000, 55000, 72000]
}
df = pd.DataFrame(data)
grouped_df = df.groupby('Department').agg({
    'Salary': ['sum', 'mean', 'max', 'min']
})
print(grouped_df)
Output:
             Salary                  
                sum    mean    max    min
Department                                
Finance      170000  85000.0  90000  80000
HR          165000  55000.0  60000  50000
IT          217000  72333.3  75000  70000
