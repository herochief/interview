# Python Question

## Potential Simple Questions

### Q1

Write a Python program find the remainder of **a** when divided by **b** 


<br>

<details>
  <summary><b>Answer</b></summary>

  ```python
a = 177
b = 5
r = a%b
print("The remainder is",r)
  ```
</details>

---

### Q2

Write a Python program that calculates the area of a circle based on the radius entered by the user

E.g \
r = 1.1 \
area = 3.8013271108436504

<br>

<details>
  <summary><b>Answer</b></summary>

  ```python
import math
r = 1.1    
area = r**2 * math.pi
print("The area is",area)    
  ```
</details>

---

### Q3

Write a Python program to display the first and last colors from the following list.

```
color_list = ["Red","Green","White" ,"Black"]
```

<br>

<details>
  <summary><b>Answer</b></summary>

  ```python
color_list = ["Red","Green","White" ,"Black"]
print(color_list[0])   
print(color_list[-1]) 
  ```
</details>

---

### Q4

Write a Python program that prompt for you name and then print your name. 

<br>

<details>
  <summary><b>Answer</b></summary>

  ```python
name = input("Please input your name: ")
print("Hello ",name)
  ```
</details>

---

### Q5

Write a Python program to determine the Factorial of a Number

<br>

<details>
  <summary><b>Answer</b></summary>

  ```python
number = int(input("number:" ))

fnum = 1
for i in range(2,number+1):
    fnum *= i 
    
print(fnum)
  ```
</details>

---

### Q6

Write a Python program to determine nth number of the fibonacci Sequence

<br>

<details>
  <summary><b>Answer</b></summary>

```python
    n_term = int(input("Which term: "))

    # first two terms
    n1, n2 = 0, 1
    count = 0

    while count < n_term:
       nth = n1 + n2

       n1 = n2
       n2 = nth
       count += 1

    print(nth)
```
</details>



## Test 2: Chinese Remainder Theorem

Lets say there is an unknown value we wish to find. However, we do know that it gives a reminder when divided by certain values.

* If divided by 3, there is a reminder of 2
* If divided by 5, there is a reminder of 3
* If divided by 7, there is a reminder of 2
* It has a digit sum of 17 (optional)

Write a script to determine the smallest potential value.

<details>
  <summary><b>Answer</b></summary>

  ```python
lst = []
for x in range(1,1000):
    if x % 3 == 2 and x % 5 ==3 and x %7 == 2:
        lst.append(x)
print(lst)
  ```
</details>

### Test 3 ###

Potential Questions for the script below.

    1. What does this script with the "guess" function do?

    2. Did you notice the several if statements, How can we improve it?

    3. How Can I change the range from [1,100] to [1,500]?

    4. Lets say I want to indicate how many attempts the player took to guess the correct answer, How would you implement it?

    5. Now I wish to personalise the range of values, where the code ask for the upper and lower limits and then apply those values to the random number range.
    
    6, Create a Check to ensure the lower limit is lower than the upper limit and if so, ask for the limits again.


```python
import random


# Define function 
def guess_the_number():
    
    num = random.randint(1,100)
    print("The System will randomly generate an integer number between 1 to 100, please guess the number within the least amount of times!")

    while True:
        guess = int(input("please input an integer："))
        
        if num == guess:
            print("Congratulations, you are right！")
            break
        if num < guess:
            print("Your number is too high, please guess again！")
        if num > guess:
            print("Your number is too low, please guess again！")

# Call the function
guess_the_number()
```
