# python_HCL_29.09.2026
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
