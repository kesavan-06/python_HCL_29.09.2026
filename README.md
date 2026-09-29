# Python_Assignment
# NAME: KESAVAN S
# REG NO: 212223060125

# PROGRAM:

## 1. Print All Prime Numbers Between a Range

**Question:**
Print all prime numbers between the given input range.

**Example Input:**

```text
20 50
```

**Code:**

```python
a, b = map(int, input().split())

for n in range(a, b + 1):
    if n < 2:
        continue

    prime = True

    for i in range(2, n):
        if n % i == 0:
            prime = False
            break

    if prime:
        print(n)
```

**Output:**

```text
23
29
31
37
41
43
47
```

---

## 2. Factorial Using Recursion

**Question:**
Find the factorial of a number using recursion.

**Example Input:**

```text
5
```

**Code:**

```python
def factorial(n):
    if n == 0 or n == 1:
        return 1

    return n * factorial(n - 1)


n = int(input())

print(factorial(n))
```

**Output:**

```text
120
```

---

## 3. Square of Numbers Using Lambda

**Question:**
Find the square of each number using a lambda function.

**Example Input:**

```text
2 3 4 5
```

**Code:**

```python
numbers = list(map(int, input().split()))

square = lambda x: x * x

for n in numbers:
    print(square(n))
```

**Output:**

```text
4
9
16
25
```

---

## 4. Find the Second Largest Element in a List

**Question:**
Find the second largest element in a list.

**Example Input:**

```text
10 5 20 8 20 15
```

**Code:**

```python
numbers = list(map(int, input().split()))

numbers = list(set(numbers))
numbers.sort()

print(numbers[-2])
```

**Output:**

```text
15
```

---

## 5. Count Frequency of Characters in a String

**Question:**
Count the frequency of each character in a string.

**Example Input:**

```text
hello
```

**Code:**

```python
s = input()

freq = {}

for ch in s:
    freq[ch] = freq.get(ch, 0) + 1

print(freq)
```

**Output:**

```text
{'h': 1, 'e': 1, 'l': 2, 'o': 1}
```

---

## 6. Calculate Area of a Circle Using Math Library

**Question:**
Calculate the area of a circle using the `math` library.

**Example Input:**

```text
5
```

**Code:**

```python
import math

r = float(input())

area = math.pi * r * r

print(area)
```

**Output:**

```text
78.53981633974483
```

---

## 7. Reverse a String Without Using Built-in Reverse

**Question:**
Reverse a string without using the built-in `reverse()` function.

**Example Input:**

```text
hello
```

**Code:**

```python
s = input()

result = ""

for i in range(len(s) - 1, -1, -1):
    result += s[i]

print(result)
```

**Output:**

```text
olleh
```

---

## 8. Remove Duplicates from a List

**Question:**
Remove duplicate elements from a list.

**Example Input:**

```text
1 2 2 3 4 4 5
```

**Code:**

```python
numbers = list(map(int, input().split()))

result = []

for n in numbers:
    if n not in result:
        result.append(n)

print(result)
```

**Output:**

```text
[1, 2, 3, 4, 5]
```

---

## 9. Merge Two Dictionaries

**Question:**
Merge two dictionaries into a single dictionary.

**Code:**

```python
d1 = {'a': 10, 'b': 20}
d2 = {'c': 30, 'd': 40}

d1.update(d2)

print(d1)
```

**Output:**

```text
{'a': 10, 'b': 20, 'c': 30, 'd': 40}
```

---

## 10. Fibonacci Series Using Recursion

**Question:**
Print the Fibonacci series using recursion.

**Example Input:**

```text
7
```

**Code:**

```python
def fibonacci(n):
    if n <= 1:
        return n

    return fibonacci(n - 1) + fibonacci(n - 2)


n = int(input())

for i in range(n):
    print(fibonacci(i), end=" ")
```

**Output:**

```text
0 1 1 2 3 5 8
```



# NUMPY_CODING

## 1. Student Marks Array

**Question:**
Create a NumPy array using the marks `[78, 65, 89, 56, 92]` and display the array along with its basic properties.

**Code:**

```python
import numpy as np

marks = np.array([78, 65, 89, 56, 92])

print("Array:", marks)
print("Dimension:", marks.ndim)
print("Shape:", marks.shape)
print("Size:", marks.size)
print("Data Type:", marks.dtype)
```

**Output:**

```text
Array: [78 65 89 56 92]
Dimension: 1
Shape: (5,)
Size: 5
Data Type: int64
```

---

## 2. Student Marks Access

**Question:**
Access and display specific student marks using NumPy indexing and slicing.

**Code:**

```python
import numpy as np

marks = np.array([72, 85, 64, 90, 76])

print("First student:", marks[0])
print("Third student:", marks[2])
print("First three students:", marks[:3])
print("Last two students:", marks[-2:])
```

**Output:**

```text
First student: 72
Third student: 64
First three students: [72 85 64]
Last two students: [90 76]
```

---

## 3. Subject-wise Marks

**Question:**
Create a NumPy array for the given marks and reshape it into a matrix representing 5 students and 3 subjects.

**Code:**

```python
import numpy as np

marks = np.array([
    78, 85, 90,
    65, 72, 80,
    88, 91, 84,
    56, 62, 70,
    95, 89, 92
])

matrix = marks.reshape(5, 3)

print(matrix)
```

**Output:**

```text
[[78 85 90]
 [65 72 80]
 [88 91 84]
 [56 62 70]
 [95 89 92]]
```

---

## 4. Internal and External Marks

**Question:**
Calculate the final marks of five students using internal and external examination marks.

**Code:**

```python
import numpy as np

internal = np.array([25, 28, 24, 27, 30])
external = np.array([60, 55, 65, 58, 62])

final = internal + external

print("Internal Marks:", internal)
print("External Marks:", external)
print("Final Marks:", final)
```

**Output:**

```text
Internal Marks: [25 28 24 27 30]
External Marks: [60 55 65 58 62]
Final Marks: [85 83 89 85 92]
```

---

## 5. Pass Percentage Analysis

**Question:**
Using NumPy Boolean masking, identify students who have secured 50 marks or above.

**Code:**

```python
import numpy as np

marks = np.array([45, 78, 56, 32, 91])

passed = marks[marks >= 50]

print("Marks:", marks)
print("Students with 50 or above:", passed)
```

**Output:**

```text
Marks: [45 78 56 32 91]
Students with 50 or above: [78 56 91]
```

---

## 6. Average Marks

**Question:**
Calculate the average marks of each student in three subjects.

**Code:**

```python
import numpy as np

marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

average = np.mean(marks, axis=1)

print("Average Marks:", average)
```

**Output:**

```text
Average Marks: [84.33333333 72.33333333 87.66666667 62.66666667 92.        ]
```

---

## 7. Class Performance Statistics

**Question:**
Find the total, average, highest, lowest, and standard deviation of the marks `[67, 82, 91, 74, 58]`.

**Code:**

```python
import numpy as np

marks = np.array([67, 82, 91, 74, 58])

print("Total:", np.sum(marks))
print("Average:", np.mean(marks))
print("Highest:", np.max(marks))
print("Lowest:", np.min(marks))
print("Standard Deviation:", np.std(marks))
```

**Output:**

```text
Total: 372
Average: 74.4
Highest: 91
Lowest: 58
Standard Deviation: 11.46472851837321
```

---

## 8. Subject-wise Performance

**Question:**
Calculate the total marks obtained in each subject using an appropriate axis operation.

**Code:**

```python
import numpy as np

marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

subject_total = np.sum(marks, axis=0)

print("Subject-wise Total:", subject_total)
```

**Output:**

```text
Subject-wise Total: [382 399 416]
```

---

## 9. Student-wise Performance

**Question:**
Calculate the total marks obtained by each student using an appropriate axis operation.

**Code:**

```python
import numpy as np

marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

student_total = np.sum(marks, axis=1)

print("Student-wise Total:", student_total)
```

**Output:**

```text
Student-wise Total: [253 217 263 188 276]
```

---

## 10. Student Ranking

**Question:**
Arrange the total marks `[245, 278, 219, 290, 256]` in order and determine the ranking of the students.

**Code:**

```python
import numpy as np

marks = np.array([245, 278, 219, 290, 256])

sorted_marks = np.sort(marks)
ranking = np.argsort(marks)[::-1]

print("Sorted Marks:", sorted_marks)
print("Student Ranking:", ranking + 1)
```

**Output:**

```text
Sorted Marks: [219 245 256 278 290]
Student Ranking: [4 2 5 1 3]
```

---

## 11. Duplicate Marks Analysis

**Question:**
Identify the unique marks obtained by the students.

**Code:**

```python
import numpy as np

marks = np.array([85, 92, 85, 76, 92])

unique_marks = np.unique(marks)

print("Marks:", marks)
print("Unique Marks:", unique_marks)
```

**Output:**

```text
Marks: [85 92 85 76 92]
Unique Marks: [76 85 92]
```

---

## 12. Missing Marks

**Question:**
Calculate the average marks without considering the missing value represented by `np.nan`.

**Code:**

```python
import numpy as np

marks = np.array([78, 85, np.nan, 92, 67])

average = np.nanmean(marks)

print("Marks:", marks)
print("Average:", average)
```

**Output:**

```text
Marks: [78. 85. nan 92. 67.]
Average: 80.5
```

---

## 13. Grade Classification

**Question:**
Classify the students into grades based on their marks.

**Grade Criteria:**

```text
90 and above → A
80–89        → B
70–79        → C
60–69        → D
Below 60     → F
```

**Code:**

```python
import numpy as np

marks = np.array([95, 82, 74, 61, 45])

grades = np.select(
    [
        marks >= 90,
        marks >= 80,
        marks >= 70,
        marks >= 60
    ],
    [
        'A',
        'B',
        'C',
        'D'
    ],
    default='F'
)

print("Marks:", marks)
print("Grades:", grades)
```

**Output:**

```text
Marks: [95 82 74 61 45]
Grades: ['A' 'B' 'C' 'D' 'F']
```

---

## 14. Random Marks Generation

**Question:**
Generate marks for five students using NumPy's random number generation functionality and perform basic statistical analysis.

**Code:**

```python
import numpy as np

np.random.seed(10)

marks = np.random.randint(0, 101, 5)

print("Generated Marks:", marks)
print("Total:", np.sum(marks))
print("Average:", np.mean(marks))
print("Highest:", np.max(marks))
print("Lowest:", np.min(marks))
```

**Output:**

```text
Generated Marks: [ 9 15 64 28 89]
Total: 205
Average: 41.0
Highest: 89
Lowest: 9
```

---

## 15. Student Performance Analysis

**Question:**
Perform a complete student performance analysis by calculating total marks, average marks, highest marks, lowest marks, and identifying students who perform above the class average.

**Code:**

```python
import numpy as np

marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

total = np.sum(marks, axis=1)
average = np.mean(marks, axis=1)

class_average = np.mean(average)

highest = np.max(marks, axis=1)
lowest = np.min(marks, axis=1)

above_average = np.where(average > class_average)[0] + 1

print("Total Marks:", total)
print("Average Marks:", average)
print("Highest Marks:", highest)
print("Lowest Marks:", lowest)
print("Class Average:", class_average)
print("Students Above Class Average:", above_average)
```

**Output:**

```text
Total Marks: [253 217 263 188 276]

Average Marks:
[84.33333333 72.33333333 87.66666667 62.66666667 92.        ]

Highest Marks: [90 80 91 70 95]

Lowest Marks: [78 65 84 56 89]

Class Average: 79.8

Students Above Class Average: [1 3 5]
```


## PYTHON_FUNCTIONS_CODING

## 1. Calculator Using Function

**Question:**
Write a function `calculate(a, b, operation)` that performs addition, subtraction, multiplication, or division based on the supplied operation.

**Example Input:**

```text
10
5
+
```

**Code:**

```python
def calculate(a, b, operation):
    if operation == "+":
        return a + b

    elif operation == "-":
        return a - b

    elif operation == "*":
        return a * b

    elif operation == "/":
        return a / b

    else:
        return "Invalid operation"


a = int(input())
b = int(input())
operation = input()

print(calculate(a, b, operation))
```

**Output:**

```text
15
```

---

## 2. Sum of Numbers Using `*args`

**Question:**
Write a function `sum_numbers(*args)` that accepts any number of arguments and returns their sum.

**Example Input:**

```text
10 20 30 40
```

**Code:**

```python
def sum_numbers(*args):
    total = 0

    for n in args:
        total += n

    return total


numbers = list(map(int, input().split()))

print(sum_numbers(*numbers))
```

**Output:**

```text
100
```

---

## 3. Employee Information Using `**kwargs`

**Question:**
Write a function `employee(**args)` that accepts employee information such as name, ID, department and salary, then displays the information.

**Code:**

```python
def employee(**args):
    for key, value in args.items():
        print(key, ":", value)


employee(
    name="Gayathri",
    ID=101,
    department="Testing",
    salary=50000
)
```

**Output:**

```text
name : Gayathri
ID : 101
department : Testing
salary : 50000
```

---

## 4. Remove Duplicates While Preserving Order

**Question:**
Write a function `remove_duplicates(lst)` that returns a list containing only unique elements while preserving their original order.

**Example Input:**

```text
1 2 2 3 4 3 5 1
```

**Code:**

```python
def remove_duplicates(lst):
    result = []

    for item in lst:
        if item not in result:
            result.append(item)

    return result


numbers = list(map(int, input().split()))

print(remove_duplicates(numbers))
```

**Output:**

```text
[1, 2, 3, 4, 5]
```

---

## 5. Sort List of Tuples Using Lambda

**Question:**
Using a lambda function, sort a list of tuples based on the second element.

**Example Input:**

```text
[(1, 5), (2, 3), (4, 1)]
```

**Code:**

```python
numbers = [(1, 5), (2, 3), (4, 1)]

result = sorted(numbers, key=lambda x: x[1])

print(result)
```

**Output:**

```text
[(4, 1), (2, 3), (1, 5)]
```
