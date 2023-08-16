
# PYTHON QUESTIONS

---
### Question 1.1: Lists and Indices

Write a Python program to display the first and last colors from the following list.

```
color_list = ["Red", "Green", "White", "Black"]
```

<br>

<details>
  <summary><b>Answer</b></summary>

  ```python
color_list = ["Red", "Green", "White", "Black"]
print(color_list[0])   
print(color_list[-1]) 
  ```
</details>


---
---
###  Question 1.2: Library and User Input

Write a Python program that calculates the area of a circle. The radius is input by the user.

<br>

<details>
  <summary><b>Answer</b></summary>

  ```python
import math
r = float(input("Enter radius of circle: "))    
area = r**2 * math.pi
print("The area is ",area)   
  ```
</details>

---
---

###  Question 1.3: Loops and Conditionals
Write a Python program to count and display the number of <u>**s**</u> in the following string.

> "Seven silly snakes slithered slowly in the sun"

<br>

<details>
  <summary><b>Answer</b></summary>

```python
for i in sentence:
    if i == 's':
        count += 1

print('There are',count,'s')
```
</details>


---
---

###  Question 1.4: Functions

Write a Python function that takes the sides of a right-angle triangle and returns the hypotenuse.

Hypotenuse formular: $c^{2}=a^{2}+b^{2}$

<br>

<details>
  <summary><b>Answer</b></summary>

```python
import math

def calculate_hypotenuse(a,b):
    c_sq = a**2 + b**2
    c = math.sqrt(c_sq)
    return c

a=3
b=4
hypotenuse = calculate_hypotenuse(a,b)
print('The Value of the is hypotenuse:')
print(hypotenuse)
```
</details>


---
---

###  Question 1.5: Dictionaries

1. Create a dictionary with keys for **name** and **age**.
2. Individually display the value for each key.

Example:
John is 15 years old.

<br>

<details>
  <summary><b>Answer</b></summary>

```python
thisdict = {
  "name": "John",
  "age": 15
}

print(thisdict['name'])
print(thisdict['age'])
```
</details>

---
---

###  Question 1.6: Classes
Write a Python class named `Rectangle`. \
This class should have two attributes: `width` and `height`. \
Show the `width` and `height`from the object.

Optional: \
Add two methods: `area()` and `perimeter()` that will return the corresponding values.

<br>

<details>
  <summary><b>Answer</b></summary>

```python
class Rectangle:
    def __init__(self,width,height):
        self.width = width
        self.height = height
    
    def area(self):
        a = self.width * self.height
        print('The area of the rectangle is', a )
        return a
    
    def perimeter(self):
        a = (self.width + self.height) * 2
        print('The perimeter of the rectangle is', a )
        return a

rect = Rectangle(5,6)

print(rect.width)
print(rect.height)
print(rect.area())
print(rect.perimeter())
```
</details>

---
---
---
---

###  Question 2.1: Factorial

Write a Python function that can calculate the factorial of a number.

Example: \
n! = 1 x 2 x 3 x.....x (n-1) x (n) 

<br>

<details>
  <summary><b>Answer</b></summary>

```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        num = 1
        for i in range(2,n+1):
            num *= i
        return num

n = int(input("Input n: "))
result = factorial(n)
print("The factorial of", n, "is", result)
```
</details>

---
---

### Question 2.2: FizzBuzz
Write a Python program to print the numbers 1 to 99 in ascending order line by line. \
However, if the number is divisible by 3, it should be replaced with "Fizz". \
If the number is divisible by 5, it should be replaced with "Buzz". \
If the number is divisible by both 3 and 5, it should be replaced with "FizzBuzz".

For example, the output should look like:

```
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
```

<br>

<details>
  <summary><b>Answer</b></summary>

```python
for i in range(1, 100):
  if i % 15 == 0:
    print("FizzBuzz")
  elif i % 3 == 0:
    print("Fizz")
```
</details>


---
---

### Question 2.3: Star Pyramid

Write a Python function that takes a value **n** and outputs a pyramid of * with **n** layers.

Example:

```
n = 5
pyramid(n)
```

Output:

```
    *    
   ***   
  *****  
 ******* 
*********
```
<br>

<details>
  <summary><b>Answer</b></summary>

```python
def pyramid(n):
    length = n * 2 -1
    for i in range(1,n+1):
        num_of_stars= (i*2-1)
        star = "*" * num_of_stars
        diff = int((length-num_of_stars)/2)
        layer = (' ' * diff)  +  star  + (' ' * diff)
        print(layer)

pyramid(5)
```
</details>

---
---
