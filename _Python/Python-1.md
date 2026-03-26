---
title: "Packages for Data Analysis"
collection: Python
permalink: /Python/Python-1/
date: 2024-03-16
---

This article introduces the fundamental packages for data analysis in Python: NumPy, Pandas, SciPy, and Matplotlib.

## [NumPy: the cornerstone of data analysis](https://numpy.org/)
As data analysts, we work with **NumPy** almost every day. It is the fundamental package for scientific computing in Python. Generally speaking, a 2‑D or 3‑D array is sufficient to handle most of the problems we encounter. Therefore, after importing raw data, I typically work with it as an ndarray.

The key advantage of using ndarray in Python is computational speed. In base Python, built‑in data structures fall into four categories: 
- three mutable types: **List**, **Dictionary**, and **Set**
- one immutable type: **Tuple**

Compared to **List**, the following are the main reasons behind the speed of **NumPy** (based on a helpful StackOverflow answer by Ferferite):[[Reference]](https://stackoverflow.com/questions/63409324/why-numpy-array-is-faster-than-list-in-python)
- An ndarray stores elements of the same data type in a densely packed memory layout. A Python list may contain mixed data types, imposing additional constraints during computation.
- **NumPy** can split a task into multiple subtasks and process them in parallel.
- **NumPy** functions are implemented in C, which makes them faster than operations on Python lists.

If you encounter speed issues in Python‑based data analysis, consider leveraging **NumPy**.

In this library, the core element is always a multidimensional array object (or derived objects such as masked arrays and matrices). **NumPy** also provides a wide range of routines for fast array operations, including mathematical, logical, shape manipulation, sorting, selecting, I/O, discrete Fourier transforms, basic linear algebra, statistical operations, random simulation, and more.

Believe it or not, once you have solved a data problem with **NumPy**, the only remaining challenge next time will be how to translate your analysis into ndarray operations. Please refer to the official documentation for detailed guidance. [[Official Reference]](https://numpy.org/doc/stable/reference.html) 

## [Pandas: specialist for data analysis and manipulation](https://pandas.pydata.org/)
**Pandas** is a fast, powerful, flexible, and easy‑to‑use open‑source data analysis and manipulation tool, built on top of the Python programming language.

You can perform all the same data analysis operations as in **R** and **Stata**. When dealing with moderately sized datasets and not requiring extreme speed, I often use **Pandas** as a Pythonic version of Excel—it is convenient and even allows you to write SQL‑style queries via the **pandasql** package. [[**pandasql**]](https://pypi.org/project/pandasql/)

For further details, consult the official documentation. [[Official Reference]](https://pandas.pydata.org/docs/reference/index.html) 