---
title: Cython intro
slideOptions:        
  theme: simple
---
# Cython intro

---

## Python Implementations
* CPython
  * Python C API https://docs.python.org/3/c-api/index.html
* pypy
  * CFFI
  * RPython

---

## Other Python Implementations
* Jython, IronPython, MicroPyton, Stackless Python
* implementation in other language: hython, CLPython, berp
* JS: Brython, pyjs, transcrypt, skulpt
* compiler: shedskin, nutika, 
* numba, pythran

---

## Similar Language
* Boo
* Nim
* Genie
* MyHDL

---

## C extensions
* ctypes
* pybind11
* SWIG

---

## Cython
* Cython is Python with C data types.
* Almost any Python code is valid in Cython
* For 
  * speed 
  * writing extensions

---

## Hello world
helloworld.pyx
```python
print("Hello")
```

---

## Setup.py
```python
from setuptools import setup
from Cython.Build import cythonize

setup(
    ext_modules = cythonize("helloworld.pyx")
)
```

---

## Compile and import

```bash
$ python setup.py build_ext --inplace
```

```python
>>> import helloworld
Hello World
```


---

```
"C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Auxiliary\Build\"vcvars64.bat
cl /Ox -Ic:\Users\tzerj\Anaconda3\envs\test\include /Tcgo.c /link /out:"go.exe" /subsystem:console /libpath:c:\Users\tzerj\Anaconda3\envs\test\libs
```
