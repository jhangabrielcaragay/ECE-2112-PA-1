# ECE-2112-PA-1

Jhan Gabriel V. Caragay | 2ECE-D

# A. WORD ROTATION PROBLEM
### **OBJECTIVE**
The first problem requires creating a function called: **rotate_word()** that accepts a non-empty string. The function should move the first character to the end while maintaining the original order and capitalization of all remaining characters.

### **DISCUSSION**
The function was first defined to accept a string.
```
def rotate_word(text):
```

In order to get the first letter of the string, it utilized indexing:
```
text[0]
```
>String indexing starts at 0.


To get the entirety of the string, it utilized slicing:
```
text[1:]
```
>```1``` indicates that the slicing starts at the second character of the string, while ```:``` separates the starting and ending positions. 


Since the goal is to include the rest of the string, the ending position is left **blank**. Adding a number after ```:``` specifies the index where the slicing will **stop**.     

>To further explain the syntax:
```text[start:stop]```

Finally, we will combine the two with a simple ```**+**``` and we will ```**return**``` to give back the result produced by the function.

```return text[1:] + text[0]```

### **OVERALL STRUCTURE**
```
def rotate_word(text):
  text[0]
  text[0]
  return text[1:] + text[0]
```

### **SAMPLE OUTPUT**

```
rotate_word("python")
'ythonp'
```

```
rotate_word("logic")
'ogicl'
```

```
rotate_word("Code")
'odeC'
```

```
rotate_word("A")
'A'
```
