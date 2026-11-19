---
updated_at: 2026-11-19T12:46:13.045-05:00
edited_seconds: 370
course:
tags:
"Lecture #": 0
Lecture Date: 2026-11-16
Week:
Created: November 16th 2026, 5:14:29 pm
---
Hub: 
Previous: [[25 — ESC180 Lecture 25]]
Next:

--- 
# Lecture Notes
## Reading Files
To read a file, we make a file object: 
```python
f = open(filename, encoding="latin1", "mode")
```
Where filename is based on the CWD or absolute path that you define. For instance, let the function be the following: 
```python
f = open("book.txt", encoding="latin-1")
text = f.read() #returns text as one big string
print(text) #returns text in book.txt
```

Note that `book.txt` is presented as the following: 
```txt
This is the contents of the text file. 
Hello!
Hello again!
```

Note that the address need to always be in terms of the current working directory, we can find it through: 
```python
import os 
print(os.getcwd()) #returns current working directory
```

Note that we can also read a file line by line; that is; 
```python
f = open("book.txt", encoding="latin-1")
first_line = f.readline() 
next_line = f.readline() #appends \n to end of strings found
```

Correspondingly, we can simply find the lines as a list: 
```python
f = open("book.txt", encoding="latin-1")
lines = f.readlines() #returns lines in book.txt as a matrix. 
print(lines)
```

### Encoding
Encoding basically provides a format in which we read a file; for instance; latin1 uses a 8-bit format; but other languages are not represented by these bits, resulting in the use of unicode. 

## Reading and Writing 
We have the following functions in Python and Reading: 
```python
f = open(filename, mode, encoding="latin1")
# mode set to "r" if you are reading 
# mode set to "w" if you are writing, overwrites pre-existing data present in the filename being opened. 
# mode set to "a" if you are appending to the end 
# both "w" and "a" creates a new file if path does not exist. 
```
* Note that you need to have mode set to `w` or `a` to write onto a file, as `r` keeps the file read-only. 
```python
s = f.write(message)
# writess the string message into the file, following the open format provided
```
For instance, we can write text into a file with the following code: 
```python
f = open("newfile.txt", "w")
f.write("this is a line\n")
f.write("this is another line\n")
f.close() 
```
Note that the `f.close()` function present is often required to force python to write the data within a buffer directly to the file. We can also reopen the file as the follow

Note that when dealing with files, we often use the following: 
```python
with open(filename, mode) as f:
	pass #stuff here 
```
As exiting this block closes the block .

For instance, if we wanted to count the number of words in a piece of text, then we can simply split the text present (using string methods) (see python string methods): 
```python
def num_words(text): 
	return len(text.split()) #return all words

def num_sentences(text): 
	text = text.replace("!",".")
	text = text.replace("?", ".")
	#... for all [punctuation
	return len(text.split(".")-1)

def num_letters(text): 
	num_letters: 
```
## Recursion 
### Factorials 
Recall that we can define the factorial as the following: 

$$
n! = n * (n-1)!
$$

We can write this as the following segment of code: 
```python
def factorial(n): 
	if n == 0: 
		return 1 
	return n*factorial(n-1) 
```
Note that this function calls itself, where we define a base case to ensure that we don't end up with a case of infinite recursion. 

### Fibonacci 
Note that we can define the following in terms of the Fibonacci Sequence: 
```python
def fib(n): 
	if n == 1 or n == 2: 
		return 1
	return fib(n-1) + fib(n-2)
```

### Checking Even