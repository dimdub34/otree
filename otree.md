# oTree - An open-source platform for behavioral research 

Dimitri DUBOIS  
[dimitri.dubois@umontpellier.fr](mailto:dimitri.dubois@umontpellier.fr)

<span style="font-size: 1.5em;font-weight: 500">Content</span>

- [Introduction](#/1)
- [Python](#/2) and [HTML](#/3)
- [Getting started with oTree](#/4)
- [Building a first oTree application](#/5)
- [Customizing models and fields](#6)
- [Managing flow and pages](#7)
- [Group and multiplayer interaction](#/8)
- [Automatic Execution and Simulations](#/9)
- [Exporting Data and Data Wrangling](#/10)
- [Role assignment, asymmetric web page sequencing and use of conditional structure in web pages](#/6)
- [Tips to improve the existing applications](#/7)
- [The admin side: rooms, payments and admin report](#/10)
- [HTML, CSS and Bootstrap](#/11)
- [Javascript](#/12)
- [Live Method](#/13)
- [Highcharts](#/14)
- [Internationalisation](#/15)
- [Tips & Tricks](#/16)

# Introduction

- **oTree** is an open-source framework built in Python.
- It is used for creating **economic games** and **surveys**.
- It is used in different fields like **economics, psychology, political science, management, finance, etc.** for running **online experiments, lab-in-the-field experiments and lab experiments**.

**Key Features:**
- Supports multiplayer interactions.
- Runs on web browsers, making it easy to use in both labs and online.
- Can be integrated with custom Python code (and JavaScript) for added flexibility.

<figure style="margin-top: 20px">
<img src="img/otree_devices.png" style="height: 200px">
</figure>


<figure style="display: inline-block">
<img src="img/leem.jpg" alt="LEEM">
    <figcaption>Lab experiment</figcaption>
</figure>


<figure style="display: inline-block">
    <img src="img/indonesie.jpg" alt="Field experiment (Indonesia)" alt="Indonésie">
    <figcaption>Lab-in-the-field experiment</figcaption>
</figure>

<figure style="display: inline-block">
    <img src="img/internet.jpg" alt="Online Experiment" alt="Internet">
    <figcaption>Online experiment</figcaption>
</figure>

**oTree is commonly used to study:**

- **Economic games with strategic interactions**: Prisoner's Dilemma, Ultimatum Game, Public Goods Game, etc.
- **Individual attitudes**: decision-making under risk and uncertainty, time preferences, pro-environmental behavior,  etc.
- **Social preferences**: fairness, trust, reciprocity, inequality aversion, etc.
- **Markets**: double auctions, etc.
- **Public policy evaluation**: taxes, subsidies, nudges, etc.


**Advantages of oTree:**

- Flexible: Create various types of experiments (e.g., economic games, surveys).
- Python-based: Allows advanced users to extend functionality.
- Open-source: Free to use, supported by a growing community.
- Cross-platform: Runs on browsers—participants only need a URL.
- Real-time interactions: Enables multiplayer interactions and instant feedback.

- Licensed under the MIT open source license
- Website: https://www.otree.org/
- Documentation: https://otree.readthedocs.io/en/latest/
- Citation: Chen, D.L., Schonger, M. & Wickens, C., 2016, "oTree - An open-source platform for laboratory, online, and field experiments", Journal of Behavioral and Experimental Finance 9, pp. 88-97

# Python

- **Python** is a high-level, interpreted and object-oriented programming language.
- Created by **Guido van Rossum** in the late 1980s and released in **1991**.
- Named after the British comedy group **Monty Python**, not the snake.
- **Design philosophy**: Emphasizes code readability, simplicity, and ease of use.

The latest stable version as of October 2024: **Python 3.12.x**.


**Key Features of Python**

- **Simple and Readable Syntax**: Easy to learn, focuses on readability.
- **Interpreted Language**: Python code is executed line by line, making it easy to debug.
- **Dynamically Typed**: No need to declare variable types, which makes coding faster and more flexible.
- **Extensive Standard Library**: Python comes with a vast range of libraries for handling everything from file I/O to web development, data processing, and machine learning.
- **Cross-Platform**: Python runs on Windows, macOS, and Linux without any modification.
- **Versatile**: Used in web development, data science, machine learning, automation, scientific computing, and more.

**Disadvantages of Python**

- **Performance**: Python is **slower** than compiled languages like C++ or Java due to its interpreted nature.
- **Mobile Development**: Python is not widely used for **mobile app development**.

## Python environment : Anaconda  

- a Python distribution that includes all the packages needed for data science
- easy to install and manage
- https://www.anaconda.com/products/individual
- download and install the distribution

<figure>
    <img src="img/anaconda.png" alt="Anaconda" width="300px" />
</figure>

## Python Interpreter

- The **Python interpreter** is a program that reads and executes Python code line by line.
- It’s available directly from the terminal with the instruction
    ```bash
    python
    ```
- The interpret Python can interpret and execute instructions directly, making it flexible for quick tests.

**JupyterLab**

- A modern Python interpreter, executed in the browser.
- It allows you to:
  - Write and execute Python code in **cells**.
  - Include **Markdown** for notes, documentation, and visual explanations.
  - Visualize outputs (like charts or data frames) **inline**.
- To start JupyterLab:
  ```bash
  jupyter-lab
  ```


## Variables and data types

- **Integer**: Whole numbers
   ```python
   x = 10
   ```
- **Float**: Numbers with decimals
  ```python
  y = 3.14
  ```
- **String**: Text data
  ```python
  name = "Alice"
  ```
- **Boolean**: True or False values
  ```python
  is_displayed = True
  ```
- **None**: Represents an absence of value
  ```python
  result = None
  ```

**List**  

- Lists are used to store multiple values in a single variable.
- Lists are **mutable** (you can change their content).

Example:
```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")  # Adds 'orange' to the list
print(fruits[0])  # Outputs: 'apple'
```

**Dictionaries**

- Dictionaries store data as key-value pairs.
- Keys are unique, and values can be of any type.

```python
player = {"name": "John", "score": 10}
print(player["name"])  # Outputs: 'John'
player["score"] += 5  # Updates score
```

## Control Flow

### Conditionals: `if`, `elif`, `else`  
Used to execute code based on certain conditions.

Example:
```python
score = 85
if score <= 80:
    print("A")
elif score <= 90:
    print("B")
else:
    print("C")
```

### Loops : `for`

Used to iterate over a sequence (like a list, tuple, or range).

Example:
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```
This will print each fruit in the list.

### The `range()` Function

Used to generate a sequence of numbers, commonly used in loops.

Basic Usage:
```python
for i in range(5):
    print(i)
```
This will print numbers from 0 to 4 (5 iterations, starting from 0).

**Parameters of range()**

- Single argument: range(stop)  
Generates numbers from 0 up to, but not including, `stop`.
```python
range(5)  # Generates [0, 1, 2, 3, 4]
```

- Two arguments: range(start, stop)  
Generates numbers from `start` up to, but not including, `stop`.
```python
range(2, 6)  # Generates [2, 3, 4, 5]
```

- Three arguments: range(start, stop, step)  
Generates numbers from `start` to `stop`, with increments of `step`.
```python
range(0, 10, 2)  # Generates [0, 2, 4, 6, 8]
```

- Negative Step: 
range() can also count backwards using a negative step:
```python
range(10, 0, -2)  # Generates [10, 8, 6, 4, 2]
```

### Loops : While

Repeats code as long as a condition is True.  
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

## Functions

- A **function** is a reusable block of code that performs a specific task.
- Functions allow you to:
  - **Encapsulate logic**: Organize your code into manageable parts.
  - **Avoid repetition**: Use the same code multiple times.
  - **Parameterize**: Pass data into the function for different use cases.

Example :
```python
def greet(name):
    return f"Hello, {name}"
```

**Calling of function**

```python
message = greet("Alice")
print(message)  # Outputs: Hello, Alice
```

### Parameters and Arguments

**Parameters**:
- Variables that are specified in the function definition.
- These allow functions to accept input data.

**Arguments**:
- The actual values you pass to the function when calling it.

Example:
```python
def add_numbers(a, b):
    return a + b

result = add_numbers(5, 3)
print(result)  # Outputs: 8
```
a and b are **parameters**, and 5 and 3 are **arguments**.

### Default arguments and keyword arguments
**Default Arguments**

You can assign a **default value** to a parameter, so it’s optional when calling the function.

```python
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}"

print(greet("Alice"))         # Outputs: Hello, Alice
print(greet("Alice", "Hi"))   # Outputs: Hi, Alice
```

**Keyword Arguments**

You can pass arguments by specifying the parameter name (makes the code more readable).

```python
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}"

print(greet(name="Alice", greeting="Good Morning"))
```

### Variable Number of Arguments

Python allows to define functions that accept a **variable number of arguments** using `*args` and `**kwargs`.

**Using `*args` (non-keyword arguments):**
```python
def multiply(*numbers):
    result = 1
    for num in numbers:
        result *= num
    return result

print(multiply(2, 3, 4))  # Outputs: 24
```

**Using `**kwargs` (keyword arguments):**
```python
def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_info(name="Alice", age=30)
```

### `lambda` function

- A **lambda function** is a small anonymous function that can have any number of arguments but only one expression.
- It is useful for short, simple operations.

Syntax:
```python
lambda arguments: expression
```

Example:
```python
add = lambda x, y: x + y
print(add(3, 5))  # Outputs: 8
```
Often used in functions like map(), filter(), or sorting lists by custom criteria.

## Classes and Objects

- Python is an **object-oriented** programming language.
- **Classes** are blueprints for creating objects (a way to bundle data and functionality together).
- **Objects** are instances of classes.

**Defining a Class:**
```python
class Player:
    def __init__(self, name, score=0):
        self.name = name
        self.score = score
```

**Creating an Object:**  
```python
p1 = Player("Alice")
print(p1.name, p1.score)  # Outputs: Alice 0
```

### Methods and Attributes

- **Attributes**: Variables that belong to an object (e.g., `self.name`, `self.score`).
- **Methods**: Functions that belong to an object (defined inside a class).

Example:
```python
class Player:
    def __init__(self, name, score=0):
        self.name = name
        self.score = score

    def increase_score(self, points):
        self.score += points

p1 = Player("Alice")
p1.increase_score(10)
print(p1.score)  # Outputs: 10
```

### Inheritance

- allows one class to inherit attributes and methods from another class.
- This helps reuse code and extend functionality.

Example:
```python
class Person:
    def __init__(self, name):
        self.name = name

class Player(Person):
    def __init__(self, name, score=0):
        super().__init__(name)
        self.score = score

p1 = Player("Alice")
print(p1.name, p1.score)  # Outputs: Alice 0
```

### Encapsulation and Polymorphism

**Encapsulation** : restricting direct access to some of an object's components.

**Polymorphism** : allows different classes to be treated as instances of the same class through inheritance.

Example of Encapsulation:
```python
class Player:
    def __init__(self, name, score=0):
        self.__score = score  # Private variable

    def get_score(self):
        return self.__score
```

## Exercices

Create an new Notebook in Jupyterlab, and for each exercice copy and paste the instructions, and write your code in the cell below.

### Exercice 1 : Basic Variables and Data Types

1. Create a variable `age` and assign it the value of your age.
2. Create a variable `name` and assign it your name.
3. Create a variable `height` that stores your height in meters (as a float).
4. Print a sentence that uses all three variables in a formatted string. Example: "My name is Alice, I'm 30 years old and 1.75 meters tall."


### Exercice 2 : Working with Lists

1. Create a list `fruits` that contains the following elements: "apple", "banana", "cherry", "date".
2. Add a new fruit to the list: "orange".
3. Remove "banana" from the list.
4. Print the number of fruits in the list.
5. Print the third fruit in the list (remember that lists are zero-indexed).

### Exercise 3: Control Flow (Conditionals)

1. Create a variable `score` and assign it a value between 0 and 100.
2. Write an if-else statement to print:
   - "Grade A" if the score is 90 or above,
   - "Grade B" if the score is between 80 and 89,
   - "Grade C" if the score is between 70 and 79,
   - "Grade D" if the score is below 70.

### Exercise 4: Loops

1. Write a for loop that prints all even numbers between 1 and 20.
2. Write a while loop that starts with `n = 10` and decreases `n` by 1 in each iteration until `n` equals 0. Print the value of `n` in each iteration.

### Exercise 5: Functions

1. Write a function `multiply(a, b)` that returns the product of two numbers `a` and `b`.
2. Write a function `is_even(n)` that returns `True` if the number `n` is even, and `False` otherwise.
3. Write a function `count_vowels(s)` that takes a string `s` and returns the number of vowels (a, e, i, o, u) in the string.

### Exercise 6: Working with Dictionaries

1. Create a dictionary `student` with the following keys: "name", "age", "grade".
   - Assign "Alice" to name, 20 to age, and "A" to grade.
2. Add a new key "ID" with a value of 12345.
3. Update the student's grade to "B".
4. Print the dictionary.

### Exercise 7: List Comprehensions

1. Create a list `numbers` that contains the numbers from 1 to 10.
2. Use a **list comprehension** to create a new list `squares` that contains the square of each number in `numbers`.
3. Use another list comprehension to create a list `evens` that contains only the even numbers from `numbers`.

## Solutions

### Exercice 1: Basic variables and Data Types
```python
age = 25  # Replace with your age  
name = "Alice"  # Replace with your name  
height = 1.75  # Replace with your height  

print(f"My name is {name}, I'm {age} years old and {height} meters tall.")


### Exercice 2: Working with Lists

```python
fruits = ["apple", "banana", "cherry", "date"]
fruits.append("orange")
fruits.remove("banana")

print(f"Number of fruits: {len(fruits)}")
print(f"The third fruit in the list is: {fruits[2]}")
```

### Exercice 3: Control flow (conditionals)

```python
score = 85  # Replace with any value between 0 and 100

if score >= 90:
    print("Grade A")
elif score >= 80:
    print("Grade B")
elif score >= 70:
    print("Grade C")
else:
    print("Grade D")
```

### Exercice 4: Loops

For loop for even numbers
```python
for i in range(2, 21, 2):
    print(i)
```

While loop
```python
n = 10
while n > 0:
    print(n)
    n -= 1
```

### Exercice 5: Functions

Function to multiply two numbers
```python
def multiply(a, b):
    return a * b

print(multiply(3, 4))  # Output: 12
```

Function to check if a number is even
```python
def is_even(n):
    return n % 2 == 0

print(is_even(5))  # Output: False
print(is_even(6))  # Output: True
```

Function to count vowels in a string
```python
def count_vowels(s):
    vowels = "aeiouAEIOU"
    count = 0
    for char in s:
        if char in vowels:
            count += 1
    return count

print(count_vowels("hello"))  # Output: 2
print(count_vowels("Python Programming"))  # Output: 4
```

### Exercice 6: Dictionaries
```python
student = {
    "name": "Alice",
    "age": 20,
    "grade": "A"
}

# Add a new key
student["ID"] = 12345

# Update the grade
student["grade"] = "B"

# Print the dictionary
print(student)
```

### Exercice 7: List-Comprehension
```python
numbers = list(range(1, 11))

# List comprehension for squares
squares = [n**2 for n in numbers]
print(squares)

# List comprehension for even numbers
evens = [n for n in numbers if n % 2 == 0]
print(evens)
```

# HTML, CSS and JavaScript

## HTML 
- **HTML** stands for **HyperText Markup Language**.
- It is the **standard markup language** used to create web pages.
- HTML structures content on the web using **elements** and **tags**.

**Basic HTML Structure:**
```html
<!DOCTYPE html>
<html>
<head>
  <title>Page Title</title>
</head>
<body>
  <h1>This is a Heading</h1>
  <p>This is a paragraph.</p>
</body>
</html>
```
HTML elements are represented by tags enclosed in < >.

### Common HTML Elements

- **Headings**: Used to define titles and subtitles on a page.
```html
  <h1>Heading 1</h1>
  <h2>Heading 2</h2>
```
- **Paragraphs**: Used to define blocks of text.
```html
<p>This is a paragraph.</p>
```
- **Links**: Used to create hyperlinks.
```html
<a href="https://www.example.com">Visit Example</a>
```
- **Images**: Used to embed images.
```html
<img src="image.jpg" alt="A description of the image">
```

- **Lists**: Used to create ordered or unordered lists.
```html
<ul>
  <li>First item</li>
  <li>Second item</li>
</ul>
```

- **Forms**: Used to collect user input.
```html
<form>
  <input type="text" name="name">
  <button type="submit">Submit</button>
</form>
```

### HTML Document Structure

- Every HTML page has the following basic structure:
  - `<!DOCTYPE html>`: Defines the document type (HTML5).
  - `<html>`: Root element, contains the entire HTML document.
  - `<head>`: Metadata, such as the title and links to external resources (CSS, scripts).
  - `<body>`: The main content of the page, including text, images, links, etc.

Example:
```html
<!DOCTYPE html>
<html>
<head>
  <title>My First HTML Page</title>
</head>
<body>
  <h1>Welcome to my page!</h1>
  <p>This is a simple HTML example.</p>
</body>
</html>
```

## CSS

- **CSS** stands for **Cascading Style Sheets**.
- CSS is used to control the **style** and **layout** of a web page.
- You can use CSS to change colors, fonts, sizes, spacing, and positioning of elements.

Example:
```css
body {
  background-color: lightblue;
}
h1 {
  color: navy;
  text-align: center;
}
```
CSS is usually written in a separate file (style.css) or within a `<style>` block in the HTML `<head>`.

### Syntax and Selectors

**Syntax:**  
A CSS rule consists of a **selector** and a **declaration block**.
  ```css
  selector {
    property: value;
  }
```

**CSS Selectors:**  
Element Selector: Targets HTML elements.
```css
p {
  color: red;
}
```
Class Selector: Targets elements with a specific class (uses `.`).
```css
.my-class {
  font-size: 18px;
}
```

ID Selector: Targets a single element with a specific ID (uses `#`).
```css
#my-id {
  background-color: yellow;
}
```
Grouping Selectors: Apply the same style to multiple elements.
```css
h1, p {
  margin: 20px;
}
```

### Inline, Internal, and External CSS

1. **Inline CSS**: Defined directly within an HTML element (not recommended for large projects).
  ```html
  <p style="color: red;">This is red text</p>
  ```
2. **Internal CSS**: Written inside a `<style>` tag in the `<head>` of the HTML document.
```html
<head>
  <style>
    p { color: red; }
  </style>
</head>
```
3. **External CSS**: Linked from a separate CSS file.
```html
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```
External CSS is the most common and scalable way to style web pages.

### Box Model

- The **box model** is a fundamental concept in CSS.
- Every HTML element is treated as a box, consisting of the following layers:
  - **Content**: The actual content (text, images, etc.).
  - **Padding**: Space between the content and the border.
  - **Border**: Surrounds the padding.
  - **Margin**: Space outside the border.

Example:
```css
div {
  width: 300px;
  padding: 20px;
  border: 5px solid black;
  margin: 10px;
}
```
Understanding the box model helps you design layouts and control spacing.

## JavaScript

- **JavaScript (JS)** is a programming language used to add **interactivity** to web pages.
- It can be used for:
  - **Manipulating HTML elements** (e.g., showing/hiding content, updating text).
  - **Handling user events** (e.g., clicks, form submissions).
  - **Performing calculations** and **dynamic updates** without refreshing the page.
- JavaScript runs directly in the browser, making it the foundation of modern web apps.

### Syntax

- JavaScript code is usually placed inside a `<script>` tag or in an external file (`script.js`).
- Variables are declared using `let` or `const`.

Example:
```javascript
let message = "Hello, World!";
console.log(message);  // Outputs: Hello, World!
```

### Basic JS Concepts

- Variables: Store values.
- Functions: Reusable blocks of code.
- Events: Actions like clicks, form submissions, or keypresses.

### DOM Manipulation with JavaScript

- **DOM (Document Object Model)** is a representation of the HTML page as objects.
- JavaScript can **manipulate** these objects to change the structure, content, and style of the page.

Example:
```html
<button onclick="changeText()">Click Me!</button>
<p id="demo">This is a paragraph.</p>

<script>
  function changeText() {
    document.querySelector("#demo").innerHTML = "Text has been changed!";
  }
</script>
```
When the button is clicked, JavaScript changes the content of the `<p>` element.

### JavaScript Events

- **Events** allow JavaScript to respond to user interactions.
- Common events include:
  - `onclick`: Triggered when an element is clicked.
  - `onmouseover`: Triggered when the mouse is over an element.
  - `onchange`: Triggered when an input field's value changes.

Example:
```html
<input type="text" onchange="alert('You changed the input!')">
<button onclick="alert('Button clicked!')">Click Me!</button>
```
JavaScript makes web pages interactive by responding to these events.

## Summary

- **HTML**: Provides the structure of a web page using elements like headings, paragraphs, links, and lists.
- **CSS**: Controls the appearance and layout of the page through styles like colors, fonts, margins, and borders.
- **JavaScript**: Adds interactivity, making web pages dynamic and responsive to user actions.

## Exercices

### Exercice 1: A Simple HTML Page

1. Create a simple HTML page with the following structure:
   - A title (`<h1>`) that says "My Webpage".
   - A paragraph (`<p>`) introducing yourself.
   - An unordered list (`<ul>`) of your 3 favorite hobbies.
   - A link (`<a>`) to a website you visit often (e.g., a news site, social media, etc.).

2. Add an image (`<img>`) to the page. You can use any image URL from the web.

### Exercise 2: Styling with CSS

1. Add some **CSS styles** to the HTML page from Exercise 1.
   - Change the background color of the page to light gray.
   - Center the text inside the `<h1>` element.
   - Set the font color of the paragraph text to dark blue.
   - Add padding and a border to the image.

2. Write the CSS in a `<style>` block inside the `<head>` of your HTML document.

### Exercise 3: Add JavaScript Interactivity

1. Add a button below the list of hobbies that says "Click Me!".
2. When the button is clicked, a **JavaScript alert** should display the message "Hello from JavaScript!".
3. Change the text of the paragraph (`<p>`) to "You clicked the button!" after the button is clicked.
4. Write the JavaScript inside a `<script>` tag at the bottom of your HTML document.

## Solutions

### Exercice 1: A simple HTML page
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Webpage</title>
</head>
<body>
  <h1>My Webpage</h1>
  <p>Hi, I'm a student learning web development!</p>
  
  <h2>My Hobbies</h2>
  <ul>
    <li>Reading</li>
    <li>Traveling</li>
    <li>Cooking</li>
  </ul>
  
  <p>Visit my favorite website: <a href="https://www.example.com">Example Website</a></p>
  
  <img src="https://via.placeholder.com/150" alt="Placeholder Image">
</body>
</html>
```

### Exercice 2: Styling with CSS

```html
<style>
    body {
      background-color: lightgray;
    }
    h1 {
      text-align: center;
    }
    p {
      color: darkblue;
    }
    img {
      padding: 10px;
      border: 2px solid black;
    }
  </style>
  ```

### Exercise 3: Add JavaScript Interactivity

The button
```html
<button onclick="sayHello()">Click Me!</button>
```

The JavaScript
```html
<script>
    function sayHello() {
      alert("Hello from JavaScript!");
      document.querySelector("p").innerHTML = "You clicked the button!";
    }
  </script>
```

# Getting Started with oTree

## Dedicated environment in Anaconda

**_With Anaconda Navigator_** 
- click on *Environments* 
- click on *Create*
- enter a name, *otree_env* for example and click on *Python*  and choose Python 3.11

**_Without Anaconda Navigator_**  

Open the Anaconda Prompt (or terminal)
- On Windows: Search for "Anaconda Prompt".
- On macOS/Linux: Use the terminal.
- Run the following command in the Anaconda Prompt or terminal:
```bash
  conda create --name otree_env python=3.11
```

## Installation of otree

In the Anaconda Prompt, activate the `otree_env` environment
```bash
conda activate otree_env
```

Install oTree with:
```bash
pip install otree
```

To check if oTree was installed correctly: 
```bash
otree --version
```
This should display the installed version of oTree.

## Creating a New oTree Project

- Run the following command to create an oTree project:
  ```bash
  otree startproject my_otree_project
  ```
This will create a folder my_otree_project with the project structure.  

Navigate to your project folder
```bash
cd my_otree_project
```
At this point, we have a basic oTree project.

## Python IDE : Pycharm

- IDE  = Integrated Development Environment
- https://www.jetbrains.com/pycharm/
- Download the Pycharm **Community version** and install it

<img src="img/pycharm.png" alt="Pycharm" style="height:200px"/>

**Intégration of the otree project in PyCharm**  

- once done, click on "new project", and in the location select the directory of your oTree project (my_otree_project)
- for the python interpreter, select "Custom environment", then "Conda environment" and click on the *browse* button to get the environment created with anaconda navigator (otree_env).

**Now PyCharm will use the correct Python version and environment for your oTree project.**

*NB : the otree_env environment is located in the anaconda folder/envs/otree_course/python.exe (or python if Linux or Mac)*

## Running the oTree Development Server

- **Start the oTree server** : Inside PyCharm's terminal or the Anaconda Prompt, run
  ```bash
  otree devserver
  ```  

- **Access the local server**: Open your web browser and go to
`http://localhost:8000`


You’ll see the oTree demo page where you can configure and run experiments.
With the development server running, you can now start building apps in your oTree project.

## Summary

1. **Created a dedicated environment** for oTree using Anaconda (`otree_env`).
2. **Installed oTree** in the environment using `pip install otree`.
3. **Created a new oTree project** using `otree startproject my_otree_project`.
4. **Installed and configured PyCharm**, linking it to the Anaconda environment.
5. **Ran the oTree development server** to test the project.

# Building The First oTree App

## oTree Project Structure

- An oTree project consists of **apps**. Each app represents a game or survey.
- **Apps** are independent and reusable components.

**Structure of an oTree Project:**
```
my_otree_project/
├── settings.py   # Project settings (apps, currency, etc.)
├── my_app/   # An individual app
│   ├── __init__.py  # Defines the logic and handles the UI
│   ├── MyPage.html  # HTML template for rendering the page
│   ├── Results.html 
└── manage.py     # Command-line tool to manage the project
``` 

## Core Components of an oTree App

1. **models**:
   - Defines the **data models** for players, groups, and subsessions.
   - Contains the rules and structure of the game (e.g., payoffs, rounds).

2. **pages**:
   - Manages the flow of the game.
   - Defines the user interface (UI) pages that participants see.
   - Controls the order of pages and interactions.

3. **templates**:
   - Contains the **HTML files** for rendering each page.
   - Allows for customization of the interface using HTML and Jinja2 templates.


*models and pages* are in the `__init__.py` file.

## Creating Your First oTree App

- **Step 1: Start a new app** : Run the following command to create a new app in your project:
  ```bash
  otree startapp my_first_app
  
  ```
  
- **Step 2: Add the app to your project**
    - Open settings.py in your project folder.
    - Add your new app to the SESSION_CONFIGS list:
```python
SESSION_CONFIGS = [
    {
        'name': 'my_first_app',
        'display_name': "My First App",
        'num_demo_participants': 2,
        'app_sequence': ['my_first_app'],
    },
]
```

## Defining the models

- **Players**, **Groups**, and **Subsessions** are the core models used to structure the game.

Example:
```python
from otree.api import *

class Subsession(BaseSubsession):
    pass

class Group(BaseGroup):
    pass

class Player(BasePlayer):
    name = models.StringField(label="What is your name?")
    age = models.IntegerField(label="How old are you?")
```

This defines a simple app where participants will enter their name and age.

## Controlling Flow

The `page_sequence` list controls the **sequence of pages** participants see during the experiment.

Example:
```python

class MyPage(Page):
    form_model = 'player'
    form_fields = ['name', 'age']

class Results(Page):
    pass

page_sequence = [MyPage, Results]
```

This example shows two pages: one where participants enter their name and age, and a second (empty) that will display the results.

## HTML Templates

- Templates are are used to render the HTML interface.

Example Template (Questionnaire.html):
```html
{{ block title }}
{{ endblock }}

{{ block content }}
  <p>Please enter your information below:</p>
  {{ formfields }}
  {{ next_button }} 
{{ endblock }}
```

The `{{ formfields }}` block renders the fields from MyPage (e.g., name, age).

## Running the oTree App

- **Step 1: Run the development server** : 
  ```bash
  otree devserver
  ```

- **Step 2: Access the app in your browser**
`http://localhost:8000`

From here, you can select your app and run it with the demo participants.

# Customizing Models and Fields

In oTree, data is structured using three main models:
  1. **Subsession**: Represents one session of the experiment.
  2. **Group**: Represents a set of participants interacting together.
  3. **Player**: Represents each participant in the experiment.

These models are defined in `__init__.py` and are subclasses of:
  - `BaseSubsession`
  - `BaseGroup`
  - `BasePlayer`

## Defining Custom Fields in Models

- Fields in oTree are used to store data for players, groups, and subsessions.
- You can define custom fields with different data types (e.g., strings, integers, currencies).

_Common Field Types_:
- **IntegerField**: Stores whole numbers.
   ```python
   score = models.IntegerField()
   ```
- **StringField**: Stores text data.
   ```python
   name = models.StringField()
    ```
- **BooleanField**: Stores True or False values.
    ```python
    student = models.BooleanField()
    ```
- **CurrencyField**: Stores monetary values (custom oTree type).
   ```python
    payoff = models.CurrencyField()
    ```

**Adding Fields to the Player Model**

```python
class Player(BasePlayer):
    name = models.StringField(label="What is your name?")
    age = models.IntegerField(label="How old are you?")
    score = models.IntegerField(initial=0)
```

- The label argument defines what participants will see on the form.
- The initial argument sets a default value (e.g., score starts at 0).

**Fields can be customized using several arguments**

- **label**: Text that appears next to the input field.
   ```python
   age = models.IntegerField(label="Your Age")
   ```
- **choices**: Provide a list of options for multiple choice fields.
    ```python
    favorite_color = models.StringField(choices=["Red", "Blue", "Green"])
    ```
- **initial**: Set a default value.
    ```python
    score = models.IntegerField(initial=0)
    ```
- **min and max**: for numeric fields.
  ```python
    age = models.IntegerField(label="Your Age", min=18, max=100)
    ```

## Using Form Fields in Pages

- To display a form field to the participant, you need to reference it in `form_fields` attribute of the corresponding class.

Example:
```python
class MyPage(Page):
    form_model = 'player'
    form_fields = ['name', 'age', 'score']
```

- **blank**: Allows a field to be left empty by participants (default is False).
If blank=True, the field can be optional.
    ```python
    age = models.IntegerField(label="Your Age", min=18, max=100, blank=True)
    ```
- **widget**: Customize the type of input field (e.g., radio buttons, sliders, etc.).
    ```python
    favorite_color = models.StringField(choices=["Red", "Blue", "Green"], widget=widgets.RadioSelectHorizontal)
    ```
By default with choices, a dropdown menu. Possible other widgets: RadioSelect, RadioSelectHorizontal.

## Exercice

- create a new application called demographics
- create the fields of the demographic questionnaire:
    - gender: woman / man
    - age
    - marital status: single, married, divorced, widowed
    - student: yes / no
    - level of study (Bac, Licence, Master, PhD)
    - field of study (Education, Sciences, Engineering, Law and Political Science, Agriculture and Food, Health, Economics and Management, Technical Studies)

# Managing Flow and Pages

- In oTree, experiments are structured into **pages** that control how participants interact with the app.
- Pages determine:
  - What is displayed to participants.
  - The sequence in which the pages appear.
  - How data is collected from participants.

Three key components of experiment flow:
1. **Pages**: Where the interaction occurs.
2. **Page Sequence**: The order of the pages.
3. **Wait Pages**: For synchronizing participants in multiplayer games.


## Controlling Page Sequence

- Pages are defined as classes that inherit from the `Page` class.
- The order in which pages are presented is determined by the `page_sequence` list.

```python
class Introduction(Page):
    pass

class Survey(Page):
    form_model = 'player'
    form_fields = ['age', 'gender']

class Results(Page):
    pass

page_sequence = [Introduction, Survey, Results]
```

- The participant will first see the Introduction page, then the Survey, and finally the Results page.
- `form_model` refers to the model (usually player, group, or subsession).
- `form_fields` contains a list of fields that the page collects from the participant.

## Adding Logic to Pages (is_displayed)

- You can control whether a page is shown to a participant using the `is_displayed` method.

Example:
```python
class ForStudent(Page):
    form_model = 'player'
    form_fields = ['level_of_study', "studied_discipline"]

    def is_displayed(player: Player):
        return player.student
```
The ForStudent page will only be displayed if the participant is a student (information that should have been collected earlier).

## Before/After Page Submission (before_next_page)

- The `before_next_page` method is used to run logic right before moving to the next page.

```python
class Choice(Page):
    form_model = 'player'
    form_fields = ['decision']

    def before_next_page(player: Player, timeout_happened):
        player.compute_payoff

class Results(Page):
    pass
```
The player's payoff is calculated before the display of the Results.

## Synchronizing Participants with Wait Pages

- In multiplayer games, participants need to be synchronized before continuing. This is done using **Wait Pages**.
- Wait pages ensure that all participants in a group reach the same point before proceeding.

```python
class WaitForGroup(WaitPage):
    pass
```
If you want the page to wait for all participants across all groups in a session, use the wait_for_all_groups attribute.

```python
class WaitForAll(WaitPage):
    wait_for_all_groups = True
```

When wait_for_all_groups = True, the Wait Page will only proceed when all groups in the session have reached the Wait Page.
This is useful in experiments where group actions affect each other, or you want to synchronize the entire session.

**You can define logic to run once all participants are ready**

```python
class WaitForGroup(WaitPage):
    def after_all_players_arrive(group: Group):
        group.compute_total_contributions()
```
The after_all_players_arrive method will execute once all players have reached the Wait Page.

if `wait_for_all_groups = True` the parameter of the `after_all_players_arrive` must be `subsession: Subsession`
```python
class WaitForAll(WaitPage):
    wait_for_all_groups = True
    
    def after_all_players_arrive(subsession: Subsession):
        subsession.compute_players_payoffs()
```

## Working with Timeout

- Pages in oTree can have time limits, allowing participants a limited amount of time to respond.

Setting a Timeout:
```python
class Choice(Page):
    form_model = 'player'
    form_fields = ['decision']
    timeout_seconds = 30
```
After 30 seconds, the page will automatically submit and move to the next one.


Use the timeout_happened argument in before_next_page to check if the page timed out.
```python
class Choice(Page):
    form_model = 'player'
    form_fields = ['decision']
    timeout_seconds = 30

    def before_next_page(player: Player, timeout_happened):
        if timeout_happened:
            player.participant._is_bot = True
            player.decision = random.randint(0, 20)
```

## Summary

-  **Pages**: Define how participants interact with your experiment.
-  **Page Sequence**: Determines the order in which pages are displayed.
- **Wait Pages**: Used to synchronize participants in multiplayer games.
- **Adding Logic**: Use `is_displayed` and `before_next_page` to control the flow.
- **Timeouts**: Limit the time participants have to answer.

## Exercice: Task with Synchronization

Create a multiplayer app where each player enters a number between 0 and 100. After all players have submitted their answers, the average number is calculated and displayed to all participants.

## Solution
Create the app
```bash
otree startapp number_game
```

**The models**
```python
class Subsession(BaseSubsession):
    average_number = models.FloatField()

    def compute_average_number(self):
        players = self.get_players()
        total = sum([p.chosen_number for p in players])
        self.average_number = total / len(players)

class Group(BaseGroup):
    pass

class Player(BasePlayer):
    chosen_number = models.IntegerField(
        label="Choose a number between 0 and 100",
        min=0, max=100)
```

**The pages**

```python
class InputPage(Page):
    form_model = 'player'
    form_fields = ['chosen_number']

class WaitForAll(WaitPage):
    wait_for_all_groups = True

    def after_all_players_arrive(subsession: Subsession):
        subsession.compute_average_number()

class Results(Page):
    pass

page_sequence = [InputPage, WaitForPlayers, Results]
```

**The templates**

InputPage
```html
{{ block title }}
Choice of a number
{{ endblock }}

{{ block content }}
{{ formfields }}
{{ next_button }}
{{ endblock }}
```

Results
```html
{{ block title }}
Results
{{ endblock }}

{{ block content }}
<p>The average number chosen by participants is {{ subsession.average_number }}.</p>
{{ next_button }}
{{ endblock }}
```

# Group and multiplayer interaction

**Illustrated with the Public Goods Game**

- In the **Public Goods Game**, participants are divided into groups.
- Each participant decides how much of their private endowment to contribute to a common good.
- The total contributions are multiplied by a factor and then shared equally among all group members.

## Flow of the Public Goods Game

**_Experiment Parameters_**:
- **Group size**: 4 players.
- **Endowment**: Each player starts with 20 tokens per round.
- **Private account**: Each token kept is worth 1 ECU (Experimental Currency Unit).
- **Public account**: Each token contributed is worth 0.5 ECU for **each group member**.
- **Rounds**: The game is repeated for 10 rounds.

**_Flow of the Experiment_**:
1. **Instructions**: Display game instructions to all players.
2. **WaitForAll**: Wait for all players to finish reading the instructions.
3. **Decision**: Players decide how much of their 20-token endowment to contribute to the public pool.
4. **WaitForGroup**: Synchronize the group after decisions are made.
5. **Results**: Display the total group contribution and individual earnings.
6. **WaitForAll**: Wait for all groups to finish viewing results.
7. **Next Round**: Repeat for 10 rounds.
8. **Final Screen**: End of experiment, display final earnings and thank participants.

## Using the Constants Class

- In oTree, the constants class (`C`) is where we define fixed parameters for the experiment, such as:
  - **Number of rounds**
  - **Players per group**
  - **Endowment**
  - **Marginal Per Capita Return (MPCR)**

```python
class Constants(BaseConstants):
    NAME_IN_URL = 'public_goods_game'
    PLAYERS_PER_GROUP = 4  # Group size
    NUM_ROUNDS = 10  # Number of rounds
    ENDOWMENT = 20  # Initial endowment for each player
    MPCR = 0.5  # Marginal Per Capita Return
```

## The `creating_session` Method

- In oTree, the **`creating_session`** method is used to initialize data at the start of the session.
- It runs once, before the first round of the experiment, and is typically used to:
  - Set initial values for fields.
  - Group participants.
  - Assign other session-wide variables.
- If the application is repeated (NUM_ROUNDS > 1) this method is called once by round.


```python
def creating_session(subsession: Subsession):
    # Group participants randomly
    subsession.group_randomly()
```

## Grouping Players

- oTree forms groups based on participant ID and the PLAYERS_PER_GROUP value.
- Participant ID are set based on the order in which they joined the session.

**_With PLAYERS_PER_GROUP = 4_**:
- The first four participants (Participant IDs 1, 2, 3, and 4) will be placed in Group 1.
- The next four participants (Participant IDs 5, 6, 7, and 8) will be placed in Group 2.
-  etc.
- These groups will remain the same for every round, provided you have multiple rounds.

In the PGG, players are randomly grouped at the start of the game and then groups stay unchanged :
- In the first round, participants are randomly grouped
- For all subsequent rounds, groups are **automatically retained** unless you explicitly re-group them.

```python
def creating_session(subsession: Subsession):
    if subsession.round_number == 1:
        subsession.group_randomly()
```

## Defining group-level fields and methods

- Each group needs to track the total contributions made by all group members.

```python
class Group(BaseGroup):
    total_contribution = models.IntegerField()
    individual_share = models.FloatField()

    def compute_total_contribution(self):
        self.total_contribution = sum([p.contribution for p in self.get_players()]))
        self.individual_share = self.total_contribution / len(self.get_players())
        # calcul of players' individual payoff
        for p in self.get_players():
            p.compute_payoff()
```

## Player contribution and individual payoff

- Each player decide how much to contribute from their endowment to the public good.
- Their remaining endowment (what they don’t contribute) will be kept as private profit.
  
```python
class Player(BasePlayer):
    keep = models.IntegerField()
    contribution = models.IntegerField(
        label="How much do you contribute to the public good ?",
        min=0, max=C.ENDOWMENT
    )
    payoff_ecu = models.FloatField()

    def compute_payoff(self):
        self.payoff_ecu = self.keep + self.group.individual_share * C.MPCR
        self.payoff = c(self.payoff_ecu * self.session.config["real_world_currency_per_point"])

## Exercice

Write the code of the public goods game.


# Automatic Execution and Simulations

## Using `before_next_page` for Automated Execution

- The `before_next_page` method can be used to automate certain actions before moving to the next page.
- The timeout_happened parameter is triggered when the experimenter clicks "Advance slowest users" in the admin interface under the Monitor tab.

```python
def before_next_page(player, timeout_happened):
    if timeout_happened:
        player.contribution = random.randint(0, C.ENDOWMENT)
    player.keep = C.ENDOWMENT - player.contribution
```

**Explanation**:
- If the timeout_happened flag is triggered (e.g., using the "Advance slowest users" button), the amount a player allocates to the public account is automatically set to a random value.
- For pages without data collection, simply clicking "Advance slowest users" will move the players to the next page without any additional action.

**How to Test**:
- Start a demo session of your experiment.
- Open a player link and navigate to the Monitor tab.
- Click "Advance slowest users" to test the page transition and observe the generated data in the Data tab.


This method helps you ensure that pages transition correctly and that data is being properly generated during automated play.

## Writing Test Scripts with `tests.py`

- You can run automated simulations in the terminal, generating data programmatically and testing the flow of your experiment.
- This allows you to simulate many players and export the generated data for analysis.

**Create a tests file**  
In the folder of your oTree app (e.g., public_goods), create a new Python file called `tests.py`.

```python
from . import *
import random
```

**Create the PlayerBot Class**
- Define a PlayerBot class, which simulates participant behavior.
- Use the play_round() method to specify the behavior for each round.

```python
class PlayerBot(Bot):
    def play_round(self):
        if self.round_number == 1:
            yield Instructions
        yield Submission(Decision, timeout_happened=True)
```

- yield: For each page in the `page_sequence`, use `yield` to submit actions.
- For data collection pages, use `Submission()` to trigger the `timeout_happened` event.
- No need to handle Wait Pages in the bot’s actions as they will be handled automatically.

**Run Tests**  

In the terminal, run the tests using the following command:
```bash
otree test public_goods
```

By default, this runs the test with the num_demo_participants defined in your session config. You can specify more players like this:
```bash
otree test public_goods 20  # Simulate 20 participants
```

**Export Simulated Data**  
To export the simulated data as a CSV, add the `--export` argument and specify the file path where you want the data saved:
```bash
otree test public_goods 20 --export C:\Users\John_Doe\Desktop\public_goods
``` 

## Exercice

Write test files for both the Public Goods Game and the socio-demographic questionnaire, then simulate data and export it.

# Exporting Data for Analysis

## Viewing data in real-time

You can view it in real-time using the oTree **admin panel**.
  
**Admin Panel Features**:
- View participants’ responses as they play the game.
- See real-time updates of contributions, payoffs, or any other data collected during the experiment.



## Session-Specific Data Export

- This method exports **all data for a specific session**, including all apps that were played during the session. 
- This is useful when you want a **complete overview** of the entire session, including all rounds and all participants.

1. **Go to the Session Tab** in the oTree Admin interface.
2. Select the session you want to export data from.
3. Click on the **Data Tab**
4. Click on the **Plain/Excel** link (bottom right of the screen) to download the CSV file.

What is Exported:
- Data from all apps that were part of that session.
- Includes:
  - **Player-level data** (e.g., contributions, decisions, payoffs).
  - **Group-level data** (e.g., total contributions, group decisions).
  - **Subsession-level data** (e.g., round numbers, session configurations).

## Application-Specific Data Export

- This method exports data for **individual apps** in your project.
- This is useful when you want to analyze data for a **single app** in isolation, without including other apps from the session.

1. **Go to the Data Tab** in the oTree Admin Interface.
2. Select the specific application from which you want to export data.
3. Click **"Download"** to export the CSV file.

What is Exported:
- Data specific to the chosen app.
- Focuses on the fields and variables defined in that app’s **Player**, **Group**, and **Subsession** models.
- Includes all rounds and participants for that app only.

## Data Wrangling - Cleaning and Preparing oTree Data

Once you've exported your CSV files from oTree, you often need to clean and organize the data before analysis.

**Common Data Wrangling Tasks**:
1. **Remove Unnecessary Columns**: 
   - Drop columns that are irrelevant to your analysis (e.g., internal ID fields or system-generated variables).

2. **Rename Columns**:
   - Rename columns to make them more meaningful or easier to work with in your analysis.
   - For example, rename `participant.label` to `participant`.

3. **Check and Correct Data Types**:
   - Ensure that columns have the correct data type (e.g., numeric columns are not mistakenly treated as strings).
   - Convert columns like `round_number` and `payoff` to their appropriate types (integer, float).

4. **Create New Variables**:
   - Sometimes you need to derive new variables from existing data.
   - Example: Calculate a **score** by summing up answers to multiple questions in a survey.

**Data Wrangling Example in Python (pandas)**

- In this example, we clean and merge data from two CSV files: **Public Goods Game data** and **Demographics data**.

**Step-by-Step Code**:

```python
import pandas as pd

# Load the Public Goods Game data
df = pd.read_csv("public_goods.csv")  # Load the CSV file
print(df.shape)  # Output the number of rows and columns
print(df.columns.to_list())  # List all column names
```
- Load the data: The pd.read_csv() function reads in the CSV file.
- Inspect the data: The shape function prints the dimensions (rows, columns), and columns.to_list() prints all the column names.

```python
# Keep only relevant columns
df = df[[columns_kept]].copy()

# Rename columns for easier manipulation
df.rename(columns={"participant.code": "participant", "session.code": "session"}, inplace=True)
df.rename(columns={c: c.replace("player.", "") for c in df.columns}, inplace=True)
```
- Keep selected columns: The list *columns_kept* defines which columns to retain. This step helps in removing unnecessary columns.
- Rename columns: We rename some columns (e.g., participant.code → participant and session.code → session) for easier handling.
- - Additionally, we simplify column names by removing the "player." prefix for player-related data.

```python
# Repeat the process for the socio-demographic data
demog = pd.read_csv("demographics.csv")  # Load the CSV file
demog = demog[[columns_kept]].copy()  # Keep relevant columns
demog.rename(columns={"participant.code": "participant", "session.code": "session"}, inplace=True)
demog.rename(columns={c: c.replace("player.", "") for c in demog.columns}, inplace=True)
```

Repeat for Demographics Data: The same process is applied to the demographics data—keep only selected columns, and rename them for consistency.

**Merge the Public Goods data and Demographics data on the participant column**
```python
df = df.merge(demog, on=["participant"])

# Optional: Save the cleaned and merged data for further analysis
df.to_csv("cleaned_data.csv", index=False)
```

Merge DataFrames: The merge() function combines the cleaned Public Goods data (df) with the Demographics data (demog) using the participant column as the key.


## Exercice

- open a jupyter-notebook, load the csv files, keep the needed columns, rename the columns and merge the files  
- if you prefer, you can prepare the data with R

# <a name="roles">Roles, sequential game and conditional structure in web pages</a>

*Practical example : the investment game*

## <a name="invest_game_description">The investment game</a>

- pairs of players
- 2 roles : trustor and trustee, 1 trustor and 1 trustee in each pair
- both roles endowed with 10 Euros (or ECUs)
- trustor chooses how many Euros/Ecus he/she sends to the trustee
- each amount sent by the trustor is tripled by the experimenter, i.e. the trustee receives 3 times the amount sent by the trustor
- the trustee sends back how many Euros/Ecus he/she wants, between zero and the receveid amount
- Trustor's payoff : 10 - amount sent + amount returned by the trustee
- Trustee's payoff : 10 + 3 x amount sent by the trustor - amount sent back to the trustor

## Roles

roles can be defined in the C class, it must end with ```_ROLE```

```python
class C(BaseConstants):
    PLAYERS_PER_GROUP = 2
    
    TRUSTOR_ROLE = "trustor"
    TRUSTEE_ROLE = "trustee
```

Roles are automatically attributed in the group: the first player in the group (```id_in_group = 1```) will have the role of trustor and the second one (```id_in_group = 2```) the role of trustee.   
The role is stored in the field "player.role" automatically created in the player class.

*Remark*  
If in the group several players must have the same role, for example 2 buyers and 2 sellers in a group of 4, this doesn't work. In that case it is necessary to assign roles with a dedicated method.

player.role can be used as a condition to display a page

```python
class DecisionTrustor(Page):
    def is_displayed(player: Player):
        return player.role == C.TRUSTOR_ROLE

    
class DecisionTrustee(Page):
    def is_displayed(player: Player):
        return player.role == C.TRUTEE_ROLE
```

## Conditional structure in the html file  

```html
<p>
    You have the role of
    {{ if player.role == C.TRUSTOR_ROLE }}
        trustor.
    {{ else }}
        trustee.
    {{ endif }}
</p>
```

- exists also ```{{ elif }}``` if needed

## Set min, max or choices of a field dynamically  

- in the investment game, the maximum the trustee can send back to the trustor is the amount she received. But this value is not known before the trustor makes her decision
- possible to set the maximum value of a field after its creation with ```def field_name_max()```

```python 
def amount_sent_back_max(player: Player):
    return player.amount_received
```

## Practice 

- write the code of the (one-shot) investment game (description [here](#/6/1))

**Help**  
- fields : amount_sent, amount_received, amount_sent_back, amount_returned
- amount_sent and amount_returned is for the trustor
- amount_received and amount_sent_back is for the trustee
- the page_sequence : [DecisionTrustor, DecisionTrustorWaitForGroup, DecisionTrustee, DecisionTrusteeWaitForGroup, Results]
- methods to create : set_amount_received, set_amount_returned, amount_sent_back_max

# <a name="tricks">Tips to improve existing applications</a>

## Put the fields in a table with a for loop in the html file

By default, if we let ```{{ formfields }}``` in the web page and there are several fields, the labels and fields are one below the other, as in the demographic application for example. To change that we can put the labels and fields in a table.

```html
<table class="table">
    {{ for field in form }}
    <tr>
        <td>{{ field.label }}</td>
        <td>{{ field }}</td>
    </tr>
    {{ endfor }}
</table>
```

Nb: ```class='table'``` is a css attribute, see chapter [HTML, CSS, bootstrap](#/11)

## Create a history

- in repeated games, like the public good game, it is a good practice to let the players consult the history of the game, i.e. the value of the variables in the past rounds
- use of a *for loop* and an html table
- two useful methods of the player class: player.in_all_rounds and player.in_previous_rounds can be called in the web page

```html
<table class="table">
    <thead>
        <tr>
            <th>Round</th>
            <th>Private account</th>
            <th>Public account</th>
            <th>Total public account</th>
            <th>Payoff</th>
        </tr>
    </thead>
    <tbody>
        {{ for p in player.in_all_rounds }}
        <tr>
            <td>{{ p.round_number }}</td>
            <td>{{ p.private_account }}</td>
            <td>{{ p.public_account }}</td>
            <td>{{ p.group.total_public_account }}</td>
            <td>{{ p.payoff }}</td>
         </tr>
        {{ endfor }}
    </tbody>
</table>
```

## Include an image in the web page

- create a subfolder in the ```_static``` directory with the name of your application 
- in the html file, inside the img tag, add static in the src attribute

```html 
<img src="{{ static 'application_name/picture_name.png' }}" />
```

- works the same way for video files and audio files, but it is better to put this kind of file elsewhere on the web and to just add the link in the src attribute

## Set a parameter in the SESSION_CONFIGS dictionnary and get it in the application

- useful when you plan to have several treatments
- for example if you want to run the public good game with a different MPCR
- either you change the value in the C class
- or you export this parameter and put it in the session configs. In that case, if you want to change the value of the MPCR, you do it in the session configs, not in the code of the application
- the change in the session configs can be done on the admin interface when creating a session
   
```python
SESSION_CONFIGS = [
    dict(
        name="public_goods",
        display_name="Public Goods Game",
        app_sequence=["public_goods"],
        num_demo_participants=4,
        mpcr=0.5
    ),
]
```

Then, in the creating_session method
```python
class Subsession(BaseSubsession):
    mpcr = models.FloatField()
    
# ADDITIONAL METHODS
def creating_session(subsession: Subsession):
    subsession.mpcr = subsession.session.config.get("mpcr", 0.5)
```

Whenever you used C.MPCR in the application, replace it with subsession.mpcr.

## Practice

- put the fields of the socio-demographic questionnaire in a table
- create an history in the public goods game application
- export the mpcr parameter in the settings file
- create a welcome application with the picture of your lab and add it in the app_sequence of the public good game

# <a name="rooms">The admin side: rooms, payments and admin report</a>

## Rooms  

- if you create a session you need to forward the url
- alternatively you can create a room
- a room is like a virtual lab, with always the same url to join

**In the settings file**, add a ```ROOMS``` list and add a dictionnary  
An item for each room (each item is a dictionnary)

```python
ROOMS = [
    dict(
        name="my_room",
        display_name="My Room",
    )
]
```

Once done, you can click on the "Rooms" tab, select the room and create a new session inside this room.

However if a participant clicks twice on the url, she opens two tabs and plays as two players.

To avoid this we restrict the access to the room to some labels : 

- a participant will have to connect and enter her label (or the label is given in the url)
- if she clicks twice on the same link she always plays as a unique player
- participant_label is one of the columns displayed in the monitor tab and in the Payments tab in the admin interface


**To create a room**   

- create a folder named ```_rooms``` at the root of your otree project
- inside this folder create a text file (myroom.txt for example)
- inside this text file, add a participant label per row. It could be whatever you want
```
lab_001
lab_002
lab_003
lab_004
```

**In the settings file**, add the key "participant_label_file" and for the value the path of the file.

```python
ROOMS = [
    dict(
        name="my_room",
        display_name="My Room",
        participant_label_file="_rooms/myroom.txt",
    )
]
```

**In the admin interface**, tab Rooms

- click on the room "My Room"
- connect clients to the room at http://127.0.0.1:8000/rooms/my_room
- clients enter a label (one of those in the text file)  


**Easy to send to a participant his personal link**

in a lab or on internet, provide directly individual links, such that  
http://127.0.0.1:8000/rooms/my_room/?participant_label=lab_001



- then wait to have the number of participants needed for the experiment, and once done, start the session
- once the session is started, open the Monitor tab to follow the players during the experiment
- once the session is finished, click on the Rooms tab, and close the room

**Practice**

- create a room
- start a session in this room

*To be tested : find you IP adress and then in terminal write ```otree devserver IP:8000``` and ask your neighbour to connect to IP:8000/rooms/your_room*

## Payments

- the tab "Payments" displays the payoff of each participant
- the value displayed is given by the variable **participant.payoff**
- it is equal to the cumulative payoff since the beginning of the session, i.e. the cumulative value of **player.payoff** (for each round of each application)
- the value can be overriden by setting player.participant.payoff = new_value
- it is the case for example if we want to pay only one round or only one application

### Pay only one round of the repeated game

- create a method and call this method just before the end of the application
- inside this method, select the paid round and set the value of this round's payoff to participant.payoff

```python
# ADDITIONAL METHODS
def set_final_payoff(player: Player):
    paid_round = random.randint(1, C.NUM_ROUNDS)
    player.participant.payoff = player.in_round(paid_round).payoff

# PAGES
class Results(Page):
    def before_next_page(player: Player, timeout_happened):
        if player.round_number == C.NUM_ROUNDS:
            set_final_payoff(player)
```

### Pay one application among several

- there exists an attribute in the participant class, called vars, which is a dictionnary, and in which you can store whatever you want
- the participant is the same in the different applications of the session, so you can access this "vars" dictionary from any application of the session
- so, in a method called at the end of each application you store the player's payoff for this application in the participant.vars dictionnary 
- create a final application that displays the payoff of each application (with an explanation text)
- within this "final" application, you randomly select the application that will actually be paid

**In each application of the experiment** : 
```python
# ADDITIONAL METHODS
def set_final_payoff(player: Player):
    paid_round = random.randint(1, C.NUM_ROUNDS)
    txt_final = f"Round {paid_round} has been randomly selected to be paid"
    player.participant.vars["app_name"] = dict(
        payoff=player.in_round(paid_round).payoff, 
        txt_final=txt_final
    )
        
# PAGES
class Results(Page):
    def before_next_page(player: Player, timeout_happened):
        if player.round_number == C.NUM_ROUNDS:
            set_final_payoff(player)
```

**In a final application** (app_sequence=["welcome", "public_goods", "investment_game", demographics", "final"]):

```python
# ADDITIONAL METHODS
def select_paid_app(subsession: Subsession):
    apps = ["public_goods", "investment_game"]  # the list of potentially paid applications
    for p in subsession.get_players():
        paid_app = random.choice(apps)
        p.participant.payoff = p.participant.vars[paid_app]["payoff"]

# PAGES
class BeforeFinalPage(WaitPage):
    wait_for_all_groups = True
    
    def after_all_players_arrive(subsession):
        select_paid_app(subsession)
        
class Final(Page):
    pass
```

### Pratice

- use the procedure to pay only one round in the public goods game application

## Admin report


- add a customized page to the admin interface, under the tab name "report"
- useful to create a customized payment page, or a page to display informations about the applications, or to display live statistics, either in a table or in a graph (with Highcharts)


Create a method **vars_for_admin_report(subsession)**, that returns a dictionnary
```python
def vars_for_admin_report(subsession: Subsession):
    infos_groups = list()
    for g in subsession.get_groups():
        trustor = g.get_player_by_role(C.TRUSTOR_ROLE)
        trustee = g.get_player_by_role(C.TRUSTEE_ROLE)
        infos_groups.append(
            dict(
                group_id=g.id_in_subsession,
                trustor=trustor.id_in_subsession,
                trustee=trustee.id_in_subsession,
                amount_sent=trustor.field_maybe_none("amount_sent"),
                amount_sent_back=trustee.field_maybe_none("amount_sent_back"),
                trustor_payoff=trustor.payoff,
                trustee_payoff=trustee.payoff
            )
        )
    return dict(infos_groups=infos_groups)
```

Create an html file name **admin_report.html**
```html
<table class="table">
    <thead>
    <tr>
        <th>Group</th>
        <th>Trustor</th>
        <th>Trustee</th>
        <th>Amount sent</th>
        <th>Amount sent back</th>
        <th>Trustor's payoff</th>
        <th>Trustee's payoff</th>
    </tr>
    </thead>
    <tbody>
    {{ for g in infos_groups }}
    <tr>
        <td>g{{ g.group_id }}</td>
        <td>p{{ g.trustor }}</td>
        <td>p{{ g.trustee }}</td>
        <td>{{ g.amount_sent }}</td>
        <td>{{ g.amount_sent_back }}</td>
        <td>{{ g.trustor_payoff }}</td>
        <td>{{ g.trustee_payoff }}</td>
    </tr>
    {{ endfor }}
    </tbody>
</table>
```

**Practice**

create the admin report for the investment game

# <a name="bootstrap">HTML, CSS and Bootstrap</a>

## HTML

- set of tags that are interpreted by the browser

**Useful tags**

- h1 to h6 are 6 levels of title
- p, br for paragraphs and break return
- table, thead, tbody, tr, th, td for tables
- ul, ol, li for list environment
- img for picture
- span, div, two kinds of blocks; span is an inline-block and div is a block


Introduction to HTML by the Mozilla fundation [here](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML) 

## CSS

- Cascading Style Sheet
- set the style of the html tags
- either in the "style" attribute of a tag 
```html
<p style="font-size: 0.8em; color: brown;">
    the sentences
</p>
```
or inside a style block
```html
<style>
    p {
        font-size: 0.8em;
        color: brown;
    }
</style>
```

### id attribute 

In the previous example, all the p of the html page are concerned. To apply the style to only one p (or tag) you must define an id to the corresponding p
```html
<p id="my_p">
    my sentence
</p>
```
and then select the id (add a # before the name of the id to let the browser knows you're searching for an id)
```html
<style>
    #my_p {
        font-size: 0.8em;
        color: brown;
    }
</style>
```

### class attribute

If it's for several p (tags) but not all of them, you define a class
```html
<p class="my_p">
    my sentence
</p>
```
and then
```html
<style>
    p.my_p {
        font-size: 0.8em;
        color: brown;
    }
</style>
```
It means ```all the paragraph of class my_p```

Main style properties

- font-family, font-size, font-weight, font-style
- color, background-color
- text-align, text-decoration
- height, width, margin, padding
- [List of all CSS properties](http://www.css-faciles.com/proprietes-css-liste-alphabetique.php)
- [Online CSS generator](https://html-css-js.com/css/generator/)

## Bootstrap

- library that defines a set of classes for many tags
- web-responsive
- [Boostrap's website](https://getbootstrap.com/docs/5.0/getting-started/introduction/)
- otree web interfaces are based on bootstrap
- you can add some nice graphical elements easily, mainly by setting value in the class attribute of the html tags (often div)


```html
<div class="card bg-light">
    <div class="card-body">
        <p>Here some sentences</p>
    </div>
</div>
```

### Main useful classes

- card: ```<div class="card">...</div>```: to place one or more paragraphs inside a frame whose background color can be defined ([doc](https://getbootstrap.com/docs/5.0/components/card/))
- ```<div class="row">...</div>```: to define a row, in wich you can set a grid with new divs and "col-x" class
- col-x: a row is divided into 12 columns, so you can set the number of cols a div may span, with ```<div class="col-6">``` for example
- look at [boostrap grid](https://getbootstrap.com/docs/5.0/layout/grid/) to understand how it works
- table: table, table-bordered, table-sm, table-stripped etc. ([doc](https://getbootstrap.com/docs/5.0/content/tables/))
- text alignement: text-justify, text-center, text-right
- text-color: text-danger, text-warning, text-info etc.
- margin: mt-1 to mt-5 for margin-top, mb-1 to mb-5 for margin-bottom, mx-1 to mx-5 for magin left and right, m-auto for margin-auto
- padding: pt-1 to pt-5 for padding-top, pb-1 to pb-5 for padding-bottom

## Pratice

- improve the web interfaces of the public goods game, by using the card div in the decision and results web pages

```html
<div class="card bg-light mb-3">
    <div class="card-title">
        <h4>The title of the card</h4>
    </div>
    <div class="card-body">
        <p>The body of the card</p>
    </div>
</div>
```

- change the history table style
```html
<table class="table table-stripped">
    <thead></thead>
    <tbody></tbody>
</table
```


# <a name="js">JavaScript</a>

- programming language interpreted and executed on the client side, by the browser
- can access to the tags and change their css properties
- can add and handle events (click for example)

Introduction to JavaScript by the mozilla fundation [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

- js can be added with a ```<script>...</script>``` tag at any place in the document
- also in event attributes of some html tags, like ```onclick``` for example
- or in a dedicated block at the bottom of the html file

```html
{{ block scripts }}
<script>
    js functions and instructions
</script>
{{ endblock }}
```

## Main js rules

- ";" at the end of each instruction
- // for one line comments and /* ... */ for multiple lines comments
- main types: Number, String, Boolean, Array and Dictionnary
- Array is like a python list, can store different types of objects
```javascript
let my_array = [1, false, "welcome"];
```
- Dictionnary is like in python: 
```javascript
let my_dict = {"key": "value"}; 
```
and you can access to the value with my_dict["key"]

Conditional structure
```javascript
if (condition_1) {
    instructions;
} else if (condition_2){
    instructions;
} else {
    instructions;
}
```

For loop
```javascript
for (let i=0; i<10; i++) {
    instructions repetead 10 times;
}

// array
for (let i in myArray)
    console.log(myArray[i]);

// or
for (let i of myArray) {
    console.log(i);  // display the value
}

// dictionnary
for (let [k, v] of Object.entries(my_dict))
    console.log(`${k}: ${v}`);
```

While
```javascript
while(condition) {
    instructions;
}
```

To create your own function
```javascript
function myFunction(arguments_needed) {
    instructions;
    return something
}
```

## The document object model (DOM)

- created by the browser once the page is loaded
- list all the tags, their attributes and their values
- the root is the "document" object
- you can open the developer tools of your browser to see it

<figure>
    <img src="img/dom.svg" alt="DOM" width=300/>
</figure>

- can be called with js
- document.title: displays or changes the title (tab name)
- console.log("text displayed in the console");

### Selection of html tags with querySelector and querySelectorAll

- querySelector returns the first element that matches the request
- querySelectorAll return an array with all the elements that match the resquest
- the request can be a tag, an id, a class etc.
- you have a list of the existing selector [here](https://www.w3.org/Style/css3-selectors-updates/WD-css3-selectors-20010126.fr.html#selectors)
- the easiest way is to set an id to the html element, and to select the element by its id, as in the example below. A ```#``` must be added to let the selector know that an id must be searched

In the html code (a hidden paragraph only displayed if needed)
```html
<p id="error_message" class="text-danger" style="visibility: hidden"></p>
```

In the script section
```html
<script>
let p_error = document.querySelector("#error_message");
p_error.innerHTML = "Please enter a value";
p_error.style.visibility = "visible";
</script>
```



### Select an otree widget and get the value

- otree sets an id to each widget, the id is ```id_field_name```, so a field "nationality" will have an id ```id_nationality```

To get the value of the selected element just add ```.value```
```javascript
let nationality = document.querySelector("#id_nationality").value;
```

For radio button, to get all the buttons
```javascript
document.querySelectorAll("input[name=field_name]");
```

and to get the checked button
```javascript
document.querySelector("input[name=field_name]:checked").value;
```

Example : 
```javascript
let is_student = document.querySelector("input[name=student]:checked").value;
```


### Practice

- run the demographic questionnaire
- on the web interface click on "open source code" or click on an element and click "inspect"
- in the browser console, try to select some elements with document.querySelector and document.querySelectorAll

## Main attributes of DOM objects

- element.value : to get the value of the element
- element.disabled : to enable / disable the element
- element.innerHTML : to add html content to the element
- element.style.visibility : hidden / visible to display / hide the element
- element.style.color, element.style.backgroundColor, element.style.fontSize, element.style.fontWeight, element.style.fontStyle ... More generally, element.style.X allows to change the css value of X

### Add an event listener to a widget  

Connects an event to a function : each widget triggers events (change, click, input etc., see the doc of the corresponding widget)   
Useful when you want to display/hide or enable/disable a widget depending on the value of another.  
Below an example with student and level_of_study

```html
<script>
    let stud_rb = document.querySelectorAll("input[name=student]");
    let stud_level = document.querySelector("#id_level_of_study");

    function enable_stud_level() {
        let stud = document.querySelector("input[name=student]:checked");
        stud_level.disabled = (stud.value === "False");
    }

    window.onload = function () {
        stud_level.disabled = true;
        for (let rb of stud_rb)
            rb.addEventListener("click", enable_stud_level);
    }
</script>
```

### Pratice

- in the demographic questionnaire, enable/disable student_level and student_discipline depending on whether the participant is/isn't a student



But if the widget is disabled no value is returned, so that if the field is mandatory it will raise an error.  
To avoid this, we can add ```blank=True``` in the field declaration (init file, class Player), and use the method 
```error_message``` in the class associated to the web page:

```python
class Questionnaire(Page):
    def error_message(player: Player, values):
        if values["student"] and values["level_of_study"] is None:
            return "You declared to be student, so you have to select your level of study."
```

make the changes in the field declaration and the class associated to the web page.

## An application with javascript : the balloon Analogue Risk Task (BART)

To measure the risk attitude of the participant

The participant clicks on a button to inject some air in a balloon (min 0, max 64). Each injection the balloon has one half probability to explode. Each injection worths 0.5€ but if the balloon explodes the participant losts every accumulated amount.

The participant must choose the number of air injection

```python
class Player(BasePlayer):
    injections = models.IntegerField()
    explosion_value = models.IntegerField()
    explosion = models.BooleanField()
    

def compute_payoff(player: Player):
    if player.explosition:
        player.payoff = 0
    else:
        player.payoff = player.injections * C.PAYOFF_PER_PUMP
    
    
class Decision(Page):
    form_model = "player"
    form_field = ["injections", "explosion_value", "explosion"]
```

On the web interface :

- a balloon picture
- a + button that increases the number of injections and a - button that decreases it
- if the participant clicks on the + button, the size of the ballon increases by 2 px
- if the participant clicks on the - button, the size of the ballon decreases by 2 px
- a text area displays the number of injections, and the payoff if the ballon doesn't explode
- once the participant validates her decision, she discovers whether the balloon explodes or not. If it does, a picture with the exploded balloon is displayed.

The pictures are available [here](http://www.duboishome.info/dimitri/cours/oTree/files/bart_pictures.zip)

Steps : 

1. a function that increases the number of injections and the size of the balloon
2. a function that decreases the number of injections and the size of the balloon
3. a connection between the + button and the increase function and a connection between the - button and the decreases function
4. a button "Validate" that randomly selects the injection at which the ballon explodes. If the explosion value is lower than or equal the number of injections chosen by the participant the ballon explodes, otherwise it doesn't explode. If the balloon explodes the participant's payoff is equal to 0. If not, the participant's payoff is equal to the number of injections x 0.5 €
5. once the result is displayed enabled the "next" button.

$\downarrow$ Help in the next slide

### Help

1. to enable / disable the next button
```javascript
document.querySelector(".otree-btn-next").disabled = True;
```

2. to select of random value between 0 and 64
```javascript
let explosion_value = Math.floor(Math.random() * (64 - 0) + 1); 
```

3. to change the size of an image
```javascript
let the_image = document.querySelector("#img_balloon");
the_image.style.width += 2;
the_image.style.height += 2;
```

4. to change an image (suppose the id of the image is img_balloon)
```javascript
let the_image = document.querySelector("#img_balloon");
the_image.src = "{{ static 'bart/exploded.png' }}";
```

$\downarrow$ to be continued in the next slide

5. to add invisible input

```html
<input type="hidden" name="explosion_value" value="">
<input type="hidden" name="explosion" value="">
```
and in javascript 
```javascript
let input_exp_val = document.querySelector("input[name=explosion_value]");
let input_exp = document.querySelector("input[name=explosion]");

input_exp_value.value = explosion_value;
input_exp = explosion_value > injections;
```


### Practice

Write the BART application

# <a name="livemethod">Live method</a>

- allows a live communication between the web page and the server
- useful for a chat application or an auction market application for example
- javascripts methods in the web page:
    + **liveSend(data)** to send data to the server (usually a dictionnary)
    + **liveRecv(data)** to receive the data from the server
- python method (in the correspond page class): ```live_method(player: Player, data)```
- this method must return a dictionnary, with as key the player (id_in_group) to send the data to and as value the data
- to send to every group members the key must be 0

html file : liveSend(data) $\rightarrow$ python file: live_method(player: Player, data) $\rightarrow$ html file : liveRecv(data)

## Example

Send a random value to the other players in the group  

In the init file
```python
class Decision(Page):
    def live_method(player: Player, data):
        print(data)  # to check
        data["sender"] = player.id_in_group
        return {0: data}
```

In the Decision.html file
```html
{{ block content }}
<button type="button" class="btn btn-secondary" onclick="send_random_value()">Send a random value</button>
{{ endblock }}

{{ block scripts }}
<script>
    function send_random_value() {
        let random_value = Math.random();
        console.log(`Send ${random_value}`);
        liveSend({random_value: random_value});
    }
    function liveRecv(data){
        console.log(`Received :`);
        for (let [k, v] of Object.entries(data))
            console.log(`${k}: ${v}`)
    }
</script>
{{ endblock }}
```

## Practice

- write a simple application (chat for example) where the player sends messages to everyone in her group

# <a name="highcharts">Highcharts</a>

- js/css library to make graphics
- website: https://www.highcharts.com/
- installation: just load the library by adding 
```html 
<script src="https://code.highcharts.com/highcharts.js"></script>`
```

Visit the Highcharts' website, and in demos select the desired graphic, and click on "edit in jsfiddle" to download the code.

## Example 

In the block content create a div
```html
<div id="graphic"></div>
```

and in the scripts block : 
```html
<script>
Highcharts.chart('graphic', {
    chart: {
        type: 'line'
    },
    title: {
        text: 'Injections dans le BART'
    },
    xAxis: {
        title: {text: "Rounds"},
        min: 0.5,
        max: 10.5,
        tickInterval: 1
    },
    yAxis: {
        title: {text: "Injections"},
        min: 0,
        max: 64,
        tickInterval: 8
    },
    series: [{
        name: 'Injections',
        data: [[1, 11], [2, 17], [3, 34], [4, 22], [5, 9], [6, 45], [7, 21], [8, 23], [9, 38], [10, 52]]
    }],
    credits: {enabled: false}
});
</script>
```

## Practice

- create an application (graph for example) and inside the page display a graph with highcharts

# <a name="i18n">Internationalisation</a>

Create a lexicon with the words or sentences translated in the different languages. For example, a file **lexicon_en.py**:

```python
class Lexicon:
    amount_sent="You have to decide the amount you sent to the trustee."
    amount_sent_back="You have to decide the amount you sent back to the trustor."
```

and a file **lexicon_fr.py**

```python
class Lexicon:
    amount_sent="Vous devez décider du montant que vous  envoyez au joueur B."
    amount_sent_back="Vous devez décider du montant que vous renvoyez au joueur A."
```

Import the language code and depending on it import the corresponding lexicon file

In the \_\_init\_\_ file in the import section

```python
from settings import LANGUAGE_CODE

if LANGUAGE_CODE == 'en':
    from .lexicon_en import Lexicon
else:
    from .lexicon_fr import Lexicon
```




In the page class you add the lexicon in the vars_for_template method
```python
class DecisionTrustor(Page):
    def vars_for_template(player: Player):
        return dict(
            language=LANGUAGE_CODE,
            lexicon=Lexicon
        )
```
and then in the html file
```html
{{ lexicon.amount_sent }}
```

For long sentences or whole paragraphs, or if some variables are needed (as ```player.payoff``` for example), it is easier to use the if statement

```html
{{ if language == "fr" }}
    <p>
        Un paragraphe en français
    </p>
    
{{ elif language == "en" }}
    <p>
        a paragraph in english.
    </p>
    
{{ endif }}
```

## Pratice

- add a language for one of the applications

# <a name="tips_and_tricks">Tips & tricks</a>

## Manual wait page

- if the experimenter wants to read the instructions aloud after subjects have read them silently, i.e. the experimenter wants to control the moment at which the next page will be displayed
- create a page without any button, so that subjects are forced to wait
- use "Advance slowest user" on the administration page (server side), in the "Monitor" tab
- by personal convention the name of this kind of page ends with "WaitMonitor".

## Display a value as a currency 

- add ```|cu``` filter to the variable

```html
<p>
    You have an endowment of {{ C.ENDOWMENT|cu }}.
</p>
```
will display "You have an endowment of €10.00".
