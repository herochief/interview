---
### Q1. Lists and Indices

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
### Q2. Math Module and User Input

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

### Q3. Loops and Conditionals

Write a Python program to print the numbers 1 to 99 in ascending order line by line. However, if the number is divisible by 3, it should be replaced with "Fizz". If the number is divisible by 5, it should be replaced with "Buzz". If the number is divisible by both 3 and 5, it should be replaced with "FizzBuzz".

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
...
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
  elif i % 5 == 0:
    print("Buzz")
  else:
    print(i)
```
</details>
or
<details>
  <summary><b>Answer</b></summary>

```python
for i in range(1, 100):
  result = ""
  
  if i % 3 == 0:
    result += "Fizz"
  if i % 5 == 0:
    result += "Buzz"
    
  if result == "":
    result = i
  print(result)
```
</details>

---

---

### Q4. Recursion or Loops

Write a Python function that can calculate the factorial of a number.

<br>

<details>
  <summary><b>Answer</b></summary>

```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)

n = int(input("Input n: "))
result = factorial(n)
print("The factorial of", n, "is", result)
  ```
</details>
or
<br>

<details>
  <summary><b>Answer</b></summary>
```python
n = int(input("Input n:"))

factorial = 1
for i in range(2, n + 1):
    factorial *= i 
    
print(factorial)
  ```
</details>

---

---

### Q5. String Operations

Write a Python function that takes a string and returns a string where every character is duplicated. For example, `"Hello"` becomes `"HHeelllloo"`.

<br>

<details>
  <summary><b>Answer</b></summary>

```python
def duplicate_characters(input_string):
    output_string = ""
    for char in input_string:
        output_string += char * 2
    return output_string

string = input("Input string: ")
result = duplicate characters(string)
print("Output string: ", result)
  ```
</details>


---

---

### Q6. Dictionaries

Write a Python function that takes a list of numbers and returns a dictionary where the keys are the numbers, and the values are tuples containing the square and cube of these numbers.

<br>

<details>
  <summary><b>Answer</b></summary>

```python
def calculate_square_cube(numbers):
    result = {}
    for num in numbers:
        square = num ** 2
        cube = num ** 3
        result[num] = (square, cube)
    return result

numbers_list = [1, 2, 3, 4, 5]
result_dict = calculate_square_cube(numbers_list)
print(result_dict)
```
</details>


---

---

### Q7. Classes

Write a Python class named `Rectangle`. This class should have two attributes: `width` and `height`. Add two methods: `area()` and `perimeter()` that will return the corresponding values.

<br>

<details>
  <summary><b>Answer</b></summary>

```python
class Rectangle:
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

    def perimeter(self):
        return 2 * (self.width + self.height)

rectangle = Rectangle(5, 3)
print("Area:", rectangle.area())
print("Perimeter:", rectangle.perimeter())
```
</details>


---

---

### Q8. Long Question 1

Write a Python program for a number guessing game. An integer will be randomly generated between 1 and 100, and the user will be prompted to make guesses. If the user guesses correctly, the game ends. Otherwise, the user will be informed whether their guess is too high or too low, and the game continues.

Optional:
- Output the total number of guesses at the end.

- The range of numbers is input by the user at the start.
    
- Check if the input range of numbers is invalid (e.g. 100 to 0). If so, prompt the user to input values again.

<br>

<details>
  <summary><b>Answer</b></summary>

```python
import random

# Define function 
def guess_the_number():
    
    num = random.randint(1, 100)
    print("The System will randomly generate an integer between 1 to 100, please guess the number!")

    while True:
        guess = int(input("Please input an integer："))
        
        if num == guess:
            print("Congratulations, you are right！")
            break
        if num < guess:
            print("Your number is too high, please guess again")
        if num > guess:
            print("Your number is too low, please guess again")

# Call the function
guess_the_number()
```
</details>

---

---

### Q9. Long Question 2

Write a Python program to return the real roots of a quadratic equation ($ax^2 + bx + c = 0$). The coefficients will be input by the user.

Optional:
- The program should be able to handle cases where $a$ is zero and where $a, b$ is zero.

- The program can find the complex roots as well.

<br>

<details>
  <summary><b>Answer</b></summary>

```python
import math

def solve_quadratic_equation():
    a = float(input("Enter the coefficient of x^2 (a): "))
    b = float(input("Enter the coefficient of x (b): "))
    c = float(input("Enter the constant term (c): "))

    # Calculate the discriminant
    discriminant = b**2 - 4*a*c

    # Check if roots are real
    if discriminant >= 0:
        # Calculate the roots
        root1 = (-b + math.sqrt(discriminant)) / (2*a)
        root2 = (-b - math.sqrt(discriminant)) / (2*a)
        print("Root 1:", root1)
        print("Root 2:", root2)
    else:
        print("No real roots exist.")

solve_quadratic_equation()
```
</details>

---

---

### Q10. Long Question 3

Write a Python program to calculate the sum of the digits of a given input integer.

Optional:
- Calculate the digital root of the input integer.

<br>

<details>
  <summary><b>Answer</b></summary>

```python
def sum_of_digits(number):
    # Convert the number to a string for iteration
    number_str = str(number)

    # Initialize a variable to store the sum
    sum_digits = 0

    # Iterate over each character in the string
    for digit in number_str:
        # Convert the character back to an integer and add it to the sum
        sum_digits += int(digit)

    return sum_digits

number = int(input("Enter a number: "))
print("Sum of digits:", sum_of_digits(number))
```
</details>

---


```python

```
