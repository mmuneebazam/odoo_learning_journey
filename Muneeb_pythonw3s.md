# muneeb #python #w3school
# Day 3 – Starting My Python Journey 🐍

With my Odoo development environment successfully configured, I decided to strengthen my Python fundamentals before diving deeper into Odoo development.

Since Odoo is built on Python, having a solid understanding of the language will help me write cleaner code, debug issues more effectively, and develop custom modules with confidence.

## Learning Resource

I am following the Python tutorial from W3Schools:

**https://www.w3schools.com/python/**

## Progress So Far

Today, I completed the following sections along with all the practice exercises:

- ✅ Python Home
- ✅ Python Classes

Completing the exercises helped me reinforce the concepts instead of just reading the documentation.

## Today's Goal

My target for today is to complete the entire Python tutorial available on W3Schools and build a strong foundation before moving on to advanced Odoo development.

## Next Section

I am now starting the **Python File Handling** section, where I will learn how to:

- Read files
- Write to files
- Create new files
- Update existing files
- Delete files

Understanding file handling is an important skill because many real-world applications, including Odoo, frequently interact with files for importing, exporting, logging, and data processing.

## Learning Mindset

Rather than rushing through the tutorials, my focus is on understanding each concept, completing the exercises, and building a strong foundation that will benefit me throughout my Odoo development journey.

Every small step brings me closer to becoming a better Python and Odoo developer. 🚀

# Day 3 (Continued) – Python Learning Progress 🐍

With my Odoo development environment successfully configured, I shifted my focus to strengthening my Python fundamentals. Since Odoo is built on Python, developing a solid understanding of the language is essential before diving into custom module development.

## Learning Resources

- **W3Schools Python Tutorial:** https://www.w3schools.com/python/
- **CodeWithHarry – Python Tutorial for Beginners:** https://www.youtube.com/watch?v=UrsmFxEIp5k

## Progress Update

Today, I completed the following topics from the W3Schools Python tutorial:

- ✅ Python File Handling
- ✅ Python Modules
- ✅ NumPy Module

Alongside the documentation, I also followed the **CodeWithHarry Python Tutorial** to reinforce my understanding through practical coding examples and detailed explanations.

## Key Concepts Learned

### Python File Handling

- Reading files
- Writing data to files
- Creating new files
- Appending data to files
- Deleting files

### Python Modules

- Importing built-in modules
- Using module functions
- Creating reusable code
- Understanding the purpose and benefits of modules

### NumPy

- Creating NumPy arrays
- Array indexing and slicing
- Performing mathematical operations on arrays
- Basic array manipulation
- Understanding why NumPy is faster and more efficient than Python lists for numerical computing

## Learning Approach

I believe that combining documentation, video tutorials, and hands-on practice is the most effective way to learn. Instead of memorizing syntax, I focus on understanding how and why each concept works by completing exercises and implementing examples.

This approach is helping me build a strong Python foundation, which will make learning Odoo development and creating custom modules much easier in the coming days.

## Current Status ✅

- ✅ Odoo 17 Development Environment Configured
- ✅ Python Basics Completed
- ✅ Python Classes Completed
- ✅ Python File Handling Completed
- ✅ Python Modules Completed
- ✅ NumPy Basics Completed
- ✅ Practiced concepts using CodeWithHarry tutorials

## Next Goal

Continue expanding my Python knowledge by exploring more advanced topics and then begin applying these concepts while developing custom modules in Odoo.

> **"A strong foundation in Python is the first step toward becoming a skilled Odoo developer."** 🚀


# Object-Oriented Programming (OOP)

## Introduction

Object-Oriented Programming (OOP) is a programming paradigm that organizes code into **classes** and **objects** instead of only functions.

Odoo is built using OOP. Every model in Odoo is a Python class that inherits from `models.Model`. Therefore, understanding OOP is essential before learning Odoo development.

---

# Learning Objectives

After completing this topic, you will be able to:

- Understand Classes and Objects
- Understand Constructors (`__init__`)
- Understand the `self` keyword
- Create Attributes and Methods
- Differentiate Class and Instance Attributes
- Understand Inheritance
- Override Methods
- Use `super()`
- Understand how OOP is used in Odoo

---

# Prerequisites

Before starting OOP, you should know:

- Variables
- Data Types
- Operators
- Conditions
- Loops
- Functions

---

# What is OOP?

OOP is a programming style where everything revolves around **objects**.

An object contains:

- Data (Attributes)
- Behaviour (Methods)

### Real-Life Example

Consider a **Car**.

Attributes:

- Brand
- Color
- Model
- Speed

Methods:

- Start
- Stop
- Accelerate
- Brake

Just like a real car, Python objects also have attributes and methods.

---

# Class

A class is a blueprint used to create objects.

### Syntax

```python
class Student:
    pass
```

Nothing happens until an object is created.

---

# Object

An object is an instance of a class.

```python
class Student:
    pass

student1 = Student()
student2 = Student()

print(type(student1))
```

### Output

```
<class '__main__.Student'>
```

Here,

- Student → Class
- student1 → Object
- student2 → Object

---

# Constructor (`__init__`)

The constructor is automatically executed whenever a new object is created.

```python
class Student:

    def __init__(self, name, age):
        self.name = name
        self.age = age

student = Student("Ali", 22)

print(student.name)
print(student.age)
```

### Output

```
Ali
22
```

---

# The `self` Keyword

`self` refers to the current object.

Example:

```python
class Student:

    def __init__(self, name):
        self.name = name
```

When we create

```python
student = Student("Ahmed")
```

Python internally executes something similar to

```python
Student.__init__(student, "Ahmed")
```

Therefore,

`self` always represents the object calling the method.

---

# Attributes

Attributes store data inside an object.

```python
class Student:

    def __init__(self, name, age):
        self.name = name
        self.age = age
```

Instance Attributes

- name
- age

---

# Methods

Methods define what an object can do.

```python
class Student:

    def __init__(self, name):
        self.name = name

    def greet(self):
        print(f"Hello {self.name}")

student = Student("Ali")
student.greet()
```

### Output

```
Hello Ali
```

---

# Instance Attributes vs Class Attributes

## Instance Attribute

Each object has its own value.

```python
class Student:

    def __init__(self, name):
        self.name = name

s1 = Student("Ali")
s2 = Student("Ahmed")

print(s1.name)
print(s2.name)
```

### Output

```
Ali
Ahmed
```

---

## Class Attribute

Shared by every object.

```python
class Student:

    school = "ABC School"

    def __init__(self, name):
        self.name = name

s1 = Student("Ali")
s2 = Student("Ahmed")

print(s1.school)
print(s2.school)
```

### Output

```
ABC School
ABC School
```

---

# Inheritance

Inheritance allows one class to reuse another class.

```python
class Animal:

    def speak(self):
        print("Animal speaks")

class Dog(Animal):
    pass

dog = Dog()
dog.speak()
```

### Output

```
Animal speaks
```

---

# Method Overriding

A child class can replace the parent's method.

```python
class Animal:

    def speak(self):
        print("Animal")

class Dog(Animal):

    def speak(self):
        print("Dog")

dog = Dog()
dog.speak()
```

### Output

```
Dog
```

---

# Using `super()`

Sometimes we want to extend the parent method instead of replacing it.

```python
class Animal:

    def speak(self):
        print("Animal")

class Dog(Animal):

    def speak(self):
        super().speak()
        print("Dog")

dog = Dog()
dog.speak()
```

### Output

```
Animal
Dog
```

---

# OOP in Odoo

Every Odoo model is a Python class.

```python
from odoo import models, fields

class Student(models.Model):
    _name = "academy.student"

    name = fields.Char()
```

Explanation

- Student → Python Class
- models.Model → Parent Class
- _name → Odoo Model Name
- fields.Char() → Field Definition

---

# Overriding Methods in Odoo

One of the most common OOP concepts in Odoo is method overriding.

```python
from odoo import api, models

class Student(models.Model):
    _inherit = "academy.student"

    @api.model
    def create(self, vals):
        record = super().create(vals)
        print("Student Created")
        return record
```

Here,

- We inherit an existing model.
- Override the create() method.
- Use super() to preserve the original functionality.

---

# Why OOP is Important in Odoo

OOP is used everywhere in Odoo.

Examples include:

- Models
- Wizards
- Controllers
- Business Logic
- Method Overriding
- Inheritance
- Recordsets

Without understanding OOP, learning Odoo becomes difficult.

---

# Common Mistakes

❌ Forgetting `self`

```python
def greet():
```

✅ Correct

```python
def greet(self):
```

---

❌ Forgetting to create an object

```python
Student.greet()
```

✅ Correct

```python
student = Student()
student.greet()
```

---

❌ Forgetting to call `super()` when extending parent behavior.

---

# Practice Exercises

## Exercise 1

Create a Book class.

Requirements

- title
- author

---

## Exercise 2

Create two Book objects.

Print their details.

---

## Exercise 3

Create a Vehicle class.

Create a Car class that inherits from Vehicle.

---

## Exercise 4

Override one method in Car.

---

## Exercise 5

Use `super()` to call the parent method.

---

## Interview Questions

### What is OOP?

### What is a Class?

### What is an Object?

### What is the purpose of `self`?

### What is a Constructor?

### Difference between Class Attribute and Instance Attribute?

### What is Inheritance?

### What is Method Overriding?

### Why do we use `super()`?

### How is OOP used in Odoo?

---

# Summary

In this chapter, you learned:

- ✅ Classes
- ✅ Objects
- ✅ Constructors
- ✅ self
- ✅ Attributes
- ✅ Methods
- ✅ Class Attributes
- ✅ Instance Attributes
- ✅ Inheritance
- ✅ Method Overriding
- ✅ super()
- ✅ OOP in Odoo

These concepts form the foundation of Odoo development.

---

# References

## Official Documentation

- Python Classes: https://docs.python.org/3/tutorial/classes.html
- Python Data Model: https://docs.python.org/3/reference/datamodel.html
- Odoo Developer Documentation: https://www.odoo.com/documentation

## W3Schools

- https://www.w3schools.com/python/python_classes.asp
- https://www.w3schools.com/python/python_inheritance.asp

## YouTube

### Corey Schafer

https://www.youtube.com/playlist?list=PL-osiE80TeTsqhIuOqKhwlXsIBIdSeYtc

### Programming with Mosh

https://www.youtube.com/watch?v=_uQrJ0TkZlc

### CodeWithHarry

https://www.youtube.com/@CodeWithHarry

### Odoo Official

https://www.youtube.com/@Odoo
