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

# B. USERNAME BUILDER PROBLEM
### **OBJECTIVE**
The second problem requires creating a function called **make_username()** that accepts two strings: a **first name** and a **last name**. The function should convert all letters to lowercase, remove any spaces, and join the first and last names using a period (.).

### **DISCUSSION**
The function was first defined to accept **two strings**.
```
def make_username(first_name, last_name):
```

It utilized a variable called ```username``` that will store the completed username.
```
username = 
```
> This allows the final result to be returned simply using ```return username```.

To convert all of the letters to lowercase, it utilized:
```
.lower()
```
> It is attached to the two strings: ```first_name``` and ```last_name```.

In order to remove the spaces in the first name, it utilized:
```
.replace(" ","")
```
> This replaces each space with **nothing** and is also attached to the two strings: ```first_name``` and ```last_name```.

in order to join the different parts together, it utilized:
```
+
```
> ```.``` was placed between two ```+``` and is between quotation marks.

Finally, We will ```return``` to give back the result produced by the function.
```
return username
```

### **OVERALL STRUCTURE**
```
def make_username(first_name, last_name):
    username = first_name.lower().replace(" ","") + "." + last_name.lower().replace(" ","")
    return username
```


### **SAMPLE OUTPUT**

```
make_username("Ada","Lovelace")
'ada.lovelace'
```

```
make_username("Alan","Turing")
'alan.turing'
```

```
make_username("Ana Maria","De Leon")
'anamaria.deleon'
```

# C. BOOKEND SWAP PROBLEM
### **OBJECTIVE**
The third problem requires creating ```swap_bookends()``` to swap the first and last elements of a list while keeping the middle elements **unchanged**.

### **DISCUSSION**

The function was first defined to accept a list through the ```items``` parameter.
```
def swap_bookends(items):
```

In order to separate the first, middle, and last elements, it utilized **extended sequence unpacking**:
```
first, *middle, last = items
```
> first stores the first element, middle stores all elements between the first and last, and last stores the last element.

To access the first element specifically, it also utilized indexing:
```
items[0]
```
> String indexing starts at ```0```.

To access the last element, it utilized:
```items[-1]```
> ```-1``` refers to the last element of the list.

To access the elements between the first and last elements, it utilized slicing:
```items[1:-1]```
> ```1``` indicates that the slicing starts at the second element, while ```-1``` indicates that it stops before the last element.

The ```first```, ```middle```, and ```last``` elements are then assigned to their respective variables:
```
first = items[0]
last = items[-1]
middle = items[1:-1]
```

To create the new list with the bookends swapped, it utilized:
```
new_list = [last] + middle + [first]
```

Finally, We will ```return``` to give back the result produced by the function.
```
return new_list
```

### **OVERALL STRUCTURE**
```
def swap_bookends(items):
    first, *middle, last = items
    first = items[0]
    last = items[-1]
    middle = items[1:-1]
    
    new_list = [last] + middle + [first]
    return new_list
```

### **SAMPLE OUTPUT**

```
swap_bookends([1, 2, 3, 4, 5, 6])
[6, 2, 3, 4, 5, 1]
```

```
swap_bookends(["red", "green", "blue"])
['blue', 'green', 'red']
```

```
swap_bookends([8, 3])
[3, 8]
```
