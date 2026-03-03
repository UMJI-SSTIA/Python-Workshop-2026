# 2026 SSTIA Python Workshop 

![Make Our Drum Pattern!](images/vecteezy_illustration-of-man-playing-drum.jpg)

At the end of this workshop, you will create a drum pattern with deep learning method in Python. Enjoy it!

## Part 1 : Introduction to Python -- Basic Python Features

Python is the most popular language in the world, which boasts a rich set of development tools and frameworks and high readability coding style. If you want to learn artificial intelligence or deep learning, Python is definitely what you will play with all the time. Even if you don't want to study these stuffs, Python is also one of the best choices to build a small project where performance does not really count. In part 1, we will cover some basic syntax of Python. But even coverring the basic content in one short workshop is not practical. So it is more recommended to learn Python yourself after the workshop and become a master of Python

Don't worry, in this workshop, we won't play with some syntax and functions that you may only encounter in the Python documentation and computer engineering lectures. Reciting the syntax is not the purpose of this workshop, We will focus more on how Python works and the basic features of Python

## Part 2 : Python OOP Tutorial -- Object-Oriented Programming

Object-Oriented Programming is the programming style. It views the components of a project as objects (instances of classes) that have attributes and methods. Generally, Python, java and C++ are commonly used with OOP (not always as they also support functional programming FP) We will learn about the features of OOP in Python -- encapsulation, inheritance and polymorphism

## Part 3 : Common Libraries Tutorial -- PyTorch and SymPy

Libraries are the toolkits for developers, so we can use high-level APIs instead of building from low-level code

[PyTorch](https://pytorch.org/) is a popular deep learning library known for its flexibility, ease of use, and dynamic execution. In the PyTorch Intro (`PT_Part1_Intro`) you will learn the basics of computations in PyTorch and how to define neural networks using either the sequential API and `torch.nn.Module`.

[SymPy](https://www.sympy.org/en/index.html) is a Python library for symbolic mathematics. It aims to become a full-featured computer algebra system (CAS) while keeping the code as simple as possible in order to be comprehensible and easily extensible. SymPy is written entirely in Python.

## Part 4 : Music Time -- Using what we learn to build a drum pattern generator!

In this part, we will use what we have learned so far to build a drum pattern generator. We will be using a "character-level Recurrent Neural Network(RNN)" to predict the next character of drum pattern in ABC notation. For more detailed about RNN, welcome to views the SSTIA deep learning workshop. Finally, we will sample from this model to generate a brand new drum pattern that has never been heard before!