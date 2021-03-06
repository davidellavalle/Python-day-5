# Table of contents:

 * [Tools](https://github.com/davidellavalle/Python-day-5#tools)
 * [Data types](https://github.com/davidellavalle/Python-day-5#data-types)
    - [Numeric: Integer - Float](https://github.com/davidellavalle/Python-day-5#numeric)
    - [Boolean](https://github.com/davidellavalle/Python-day-5#boolean)
    - [Sequential: List - Tuple - String](https://github.com/davidellavalle/Python-day-5#sequential)
    - [Container: Set - Dictionary](https://github.com/davidellavalle/Python-day-5#container)
 * [Data Type - How to find it](https://github.com/davidellavalle/Python-day-5#how-to-find-out-the-data-type)
 * [Print and the main escape sequences](https://github.com/davidellavalle/Python-day-5#how-to-print-your-result)
 * [Python Operators](https://github.com/davidellavalle/Python-day-5#python-operators)
    - [= vs ==](https://github.com/davidellavalle/Python-day-5#-vs--and-the-other-comparison-operators)
    - [Index](https://github.com/davidellavalle/Python-day-5#index)
    - [Slices](https://github.com/davidellavalle/Python-day-5#slices)
    - [Length](https://github.com/davidellavalle/Python-day-5#length)
    - [Enumerate](https://github.com/davidellavalle/Python-day-5#enumerate)
    - [In](https://github.com/davidellavalle/Python-day-5#in)
    - [Count](https://github.com/davidellavalle/Python-day-5#count)
    - [Input](https://github.com/davidellavalle/Python-day-5#input)
* [Conditionals - Decision Making](https://github.com/davidellavalle/Python-day-5#conditionals---decision-making)
    - [The if Statement](https://github.com/davidellavalle/Python-day-5#the-if-statement)
    - [The if else Statement](https://github.com/davidellavalle/Python-day-5#the-if-else-statement)   
    - [Chained conditionals](https://github.com/davidellavalle/Python-day-5#chained-conditionals)
    - [Nested conditionals](https://github.com/davidellavalle/Python-day-5#nested-conditionals)
* [Working with loops](https://github.com/davidellavalle/Python-day-5#working-with-loops)
    - [The for loop](https://github.com/davidellavalle/Python-day-5#the-for-loop)
    - [Break](https://github.com/davidellavalle/Python-day-5#break)
    - [Continue](https://github.com/davidellavalle/Python-day-5#continue)
    - [TBF - Nested Loops for Nested Data](https://github.com/davidellavalle/Python-day-5#nested-loops-for-nested-data)
* [Function](https://github.com/davidellavalle/Python-day-5#function)
* [Excercises and solutions](https://github.com/davidellavalle/Python-day-5#excercise-and-solutions)

* [How to create a Readme Github File](https://github.com/davidellavalle/Python-day-5#how-to-create-a-github-readme-file)

# Python Day 5

## Tools

* Github - [video tutorial](https://www.youtube.com/watch?v=XIlxdG6bGU0&feature=emb_title)
* Visual Studio Code - 
    * new file - it must contain the **.ipynb** to be recognized as python paper work
* Link Github with VSC - [tutorial](https://www.youtube.com/watch?v=XIlxdG6bGU0&feature=emb_title)
* Anaconda - It’s an open-source package management system and environment management system, primarily for Python programs.
It could happen that the installed version of a programm in Anaconda is outdated, in taht case I would need to change it:
  * In Anaconda environments check what is the current version installed
  * Look for the codes to install newest versin of the programm and let it run on Anaconda prompt 

A computer program is a sequence of instructions that specifies how to perform a computation.
* **input** - Get data from the keyboard, a file, or some other device.
* **output** - Display data on the screen or send data to a file or other device.
* **assignment** - Set the value of a storage location denoted by a variable name.
* **math and logic** - Perform basic mathematical operations like addition, and multiplication, and logical operations like and, or, and not.
* **conditional execution** - Check for certain conditions and execute the appropriate sequence of statements.
* **repetition** - Perform some action repeatedly, usually with some variation.
* **Debugging** – removing Bugs -  Three kinds of errors can occur in a program: syntax errors, runtime errors, and semantic errors.

## **Data types**

![data types](https://media.geeksforgeeks.org/wp-content/uploads/20191023173512/Python-data-structure.jpg)

Data types [guide](https://dsft.code-data-ai.com/data-types-python/)

### **Numeric**

#### **Integer**

1 2 3 4 -1 -2 -3 -4…..  
This value is represented by **int class**. It contains positive or negative whole numbers (without fraction or decimal). In Python there is no limit to how long an interger value can be.

#### **Float**

1,3  1,4  1,6  5,4   6,4   -3,4  -4,3   
This value is represented by **float class**. It is a real number with floating point representation. It is specified by a decimal point. Optionally, the character e or E followed by a positive or negative integer may be appended to specify scientific notation.

### **Boolean**

This is a value that expresses a truth value (which can be **either true or false**) 
```python
>>> 5 == 5
True
>>> 5 == 6
False
```

### **Sequential**

#### **List**

A list is created by placing all the items (elements) inside a square bracket [ ], separated by commas. It doesn't need to be homogeneous but can contain Integers, Strings or Objects at the time. List are mutable and can be changed after their creation.  
The elements in a list are Indexed and **0 is the first index** -> this means that the last element will be n-1 (eg. 25 elements in the list, index 0:24) 

**Some of the most common Lists methods:** (Methods act on the values of an object (Strings, lists, and tuples)
* append() - Add an element to the end of the list
* extend() - Add all elements of a list to the another list
* insert() - Insert an item at the defined index
* remove() - Removes an item from the list
* pop() - Removes and returns an element at the given index
* clear() - Removes all items from the list
* index() - Returns the index of the first matched item
* count() - Returns the count of number of items passed as an argument
* sort() - Sort items in a list in ascending order
* reverse() - Reverse the order of items in the list
* copy() - Returns a shallow copy of the list

```python
>>> mylist = []
>>> mylist.append('this')
>>> mylist
['this']
>>> mylist.insert(1, 'thing')
>>> mylist
['this', 'thing']
>>> mylist.remove('thing')
>>> mylist
['this']
```
how to remove brackets from sublist - **FLATTENED**
```
>>> list_of_lists = [[180.0, 1, 2, 3], [173.8], [164.2], [156.5], [147.2], [138.2]] 
>>> flattened  = [val for sublist in list_of_lists for val in sublist] 
>>> flattened  
[180.0, 1, 2, 3, 173.8, 164.2, 156.5, 147.2,138.2]
```

#### **Tuple**
A Tuple is created by placing all the items (elements) inside a round bracket ( ). It is unchangeable, deletion or Updation of a tuple is not allowed.. In Dictionary we can create keys using tuples  
Indexes works as per LIST: with positive and negative indexes [1] [2] [-1] [-2]  or with range of indexes [2:5] [-3:-1]


```python
thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(thistuple[-4:-1])
('orange', 'kiwi', 'melon')


```
**Unchangeability workaround**: you can convert the tuple into a list, change the list, and convert the list back into a tuple.
```python
y = list(x)
y[1] = "kiwi"
x = tuple(y)
print(x)
("apple", "kiwi", "cherry")
```

#### **String**

A string is a collection of one or more characters put in a single quote, double-quote (Double quotes can contain singles) or triple quote (can even span multiple lines)
```python
"Ben's bike is broken!"
>>> message = """This message will
... span several
... lines."""
```

**Some of the most common string methods:**
* s.lower(), s.upper() — returns the lowercase or uppercase version of the string   
* s.isalpha()/s.isdigit()/s.isspace()… — tests if all the string chars are in the various character classes  
* s.startswith(‘ai’), s.endswith(‘ai’) — tests if the string starts or ends with the given ai strin  
* s.find(‘other’) — searches for the given other string (not a regular expression) within s, and returns the first index where it begins or -1 if not found  
* s.replace(‘old’, ‘new’) — returns a string where all occurrences of ‘old’ have been replaced by ‘new’ 

### **Container**

#### **Set**

Set is an unordered collection of data type that is **iterable, mutable** and has no duplicate elements (**Uniques**).  
A Set is created by placing all the items (elements) inside curly brackets {}
The major advantage of using a set, as opposed to a list, is that it has a highly optimized method for checking whether a specific element is contained in the set.
**Set do not support INDEXING**

```python
Set()
set1 = set("CodeDataAI")  
print(set1)
{'o', 'D', 'a', 'A', 'e', 't', 'I', 'd', 'C'}

set1 = set(["Code", "Data", "Code"])  
print(set1)
{'Data', 'Code'}
```
Adding and removing elements to a Set - 
* set.add
* set.update
* set.remove
* discard

#### **Dictionary**

Dictionary is an unordered collection of data values, used to store data values like a map.Unlike other Data Types that hold only single value as an element, Dictionary holds key:value pair.

---

### How to find out the data Type

```python
>>> type("Hello, World!")
<class 'str'>
>>> type(17)
<class 'int'>
```

### How to convert the data Type

float to integer = int(3.14) -> 3  
integer to float = float(3) -> 3.0  
string to integer = int("123") -> 123  
......

### How to print your result

```python
>>> print("Hello, World!")
Hello, World!
>>> print('a', 'b', 'c', 'd')
a b c d
>>> print('a', 'b', 'c', 'd', sep='##', end='!!')
a##b##c##d!!>>>
```
Escape sequence can be used to modify the format  
```
\\      Backslash (\)  
\'      Single quote (')  
\"      Double quote (")  
\b      Backspace  
\n      Linefeed  
\t      Tab  
```
```python
>>> print("Line 1\n\n\nLine 5")
Line 1


Line 5
>>>
```

---

## Python Operators
Operators are special tokens that represent computations like addition, multiplication and division. The values the operator uses are called operands.  
Operators follow the rule of PEMDAS - Parenthese, Exponentiation, Multiplication and both Division, than Addition and Subtraction  
The main Python Operators can be found here: https://www.w3schools.com/python/python_operators.asp

### = vs == and the other comparison operators
= assignment operator
== equal sign
```python
x != y       # x is not equal to y
x > y        # x is greater than y
x < y        # x is less than y
x >= y       # x is greater than or equal to y
x <= y       # x is less than or equal to y
```

### *Index*

The indexing operator ([ ]) selects a single element from a sequence. The expression inside brackets is called the index, and must be an integer value. The index indicates which element to select, hence its name.
```python
>>> fruits = ['apples', 'cherries', 'pears']
>>> fruits[0]
'apples'
>>> pairs = [('cheese', 'queso'), ('red', 'rojo'), ('school', 'escuela')]
>>> pairs[2]
('school', 'escuela')
```

### *Slices*

Like with indexing, we use square brackets ([ ]) as the slice operator, but instead of one integer value inside we have two, seperated by a colon (:):
```python
>>> singers = "Peter, Paul, and Mary"
>>> singers[0:5]
'Peter'
```

### *Length*

With lists and tuples, len returns the number of elements in the sequence
```python
>>> len((2, 4, 6, 8, 10, 12))
6
>>> pairs = [('cheese', 'queso'), ('red', 'rojo'), ('school', 'escuela')]
>>> len(pairs)
3
```
### *Enumerate*

I can find index and value
```python
fruits = ['apples', 'bananas', 'blueberries', 'oranges', 'mangos']

for index, fruit in enumerate(fruits):
    print("The fruit, " + fruit + ", is in position " + str(index) + ".")
```

### *In*
The in operator returns whether a given element is contained in a list or tuple
```python
>>> stuff = ['this', 'that', 'these', 'those']
>>> 'this' in stuff
True
```

### *Count*

The count operator counts how many times the selected element is present in a List, Tuple
```python
>>> list = ['this', 'that', 'these', 'those']
>>> list.count('this')
1
```

### *Input*

This function allows the user to import his input
```python
name = input("Please enter your name: ")
```

----

## Conditionals - Decision Making  

There comes a point in our life where we need to decide what steps should be taken and based on that we decide our next decisions. In programming, we often have this similar situation where we need to decide which block of code should be executed based on a condition.Decisions like these are required everywhere in programming and they decide the direction of flow of program execution. Python has the following decision-making statements:

![ifs](https://camo.githubusercontent.com/ff055b9fc456c339329742d7cd4cc4e44fb37c287e5d2ad3dc2c71c0d1e05323/68747470733a2f2f6d656469612e6765656b73666f726765656b732e6f72672f77702d636f6e74656e742f75706c6f6164732f32303230303332363136323233372f6e65737465642d6966312e6a7067)

### The *if* Statement

This is a compound statement which means it has a HEADER and a BODY.  **"IF boolean expression:"**

* The colon (:) is significant and required. It separates the header of the compound statement from the body.
* The line after the colon must be indented. It is standard in Python to use four spaces for indenting.
* All lines indented the same amount after the colon will be executed whenever the BOOLEAN_EXPRESSION is true.
```
food = 'spam'

if food == 'spam':
    print('Ummmm, my favorite!')
    print('I feel like saying it 100 times...')
    print(100 * (food + '! '))
```

### The *if else* Statement

It is frequently the case that you want one thing to happen when a condition it true, and something else to happen when it is false
```
if food == 'spam':
    print('Ummmm, my favorite!')
else:
    print("No, I won't have it. I want spam!")
```

### Chained conditionals

```
if x < y:
    STATEMENTS_A
elif x > y:
    STATEMENTS_B
else:
    STATEMENTS_C
```

### Nested conditionals

```
if x < y:
    STATEMENTS_A
else:
    if x > y:
        STATEMENTS_B
    else:
        STATEMENTS_C
```

## Working with loops

Computers are often used to automate repetitive tasks. Repeating identical or similar tasks without making errors is something that computers do well and people do poorly.

Repeated execution of a set of statements is called iteration. Python has two statements for iteration – **for and while**

### The *for* loop

It is a flow so called because it loops back around to the top after each iteration. The for loop processes each item in a sequence, so it is used with Python’s sequence data types - strings, lists, and tuples. Each item in turn is (re-)assigned to the loop variable, and the body of the loop is executed.

```
for friend in ['Margot', 'Kathryn', 'Prisila']:
    invitation = "Hi " + friend + ".  Please come to my party on Saturday!"
    print(invitation)
```
Often times you will want ***a loop that iterates a given number of times***, or that iterates over a given sequence of numbers. The ***range function*** come in handy for that.
```
for i in range(5):       # range(2,7) numbers 2-3-4-5-6   
    print('i is now:', i)

Output:
i is now 0
i is now 1
i is now 2
i is now 3
i is now 4
```

### Break
The break statement is used to immediately leave the body of its loop. The next statement to be executed is the first one after the body:
```
for i in [12, 16, 17, 24, 29]:
    if i % 2 == 1:  # if the number is odd
        break        # immediately exit the loop
    print(i)
print("done")

Output:

12
16
done
```

### Continue

Skip the rest of the body for that iteration but carry on running for the remaining iterations
```
for i in [12, 16, 17, 24, 29, 30]:
    if i % 2 == 1:     # if the number is odd
        print("Found!")
        continue        # don't process it
    print(i)
12
16
Found!
24
30
```

### Nested Loops for Nested Data

````
nums = [1,2,3,4]

for num in nums:
    for letter in "abc":
        print(num, letter)

1a
1b
1c
2a
2b
...
4c
````
----

### While loop

The for loop iterates through a certain number of values but WHILE LOOP will continue going until a certain condition is met
````
x = 0

while x<10:
    print(x)
    x +=1 # this way the x will increment and at one point the condition will be met
```` 

Note : Ctrl + C to stop the loop in case of infite loop.

## Function

A function is a block of organized, reusable code that is used to perform a single, specific task. Functions provide better modularity for your application and a high degree of code reusability.
A function is a named sequence of statements that performs a desired operation. It is a compound statement, header (def e termina con colon:) and body indented
* I can generate any name but doo not use a Keyword
* Use as many statements as needed
* RETURN to cease execution of statements (without Return the system will return NONE as value)
* All other statements after RETURN won't be executed (**dead code**)

I know already many Python built-in functions like print(),len(), sum() etc. At the same time you can also create your own functions. These functions are called user-defined functions.
* Quick [guide](https://www.programiz.com/python-programming/function) to start with Function.
* Conceptual [guide](https://inst.eecs.berkeley.edu/~cs61a/sp12/book/functions.html) how function works. (Section 1.1 can be skipped)

```
def NAME( LIST OF PARAMETERS ):
    STATEMENTS
```
```
def f(x):
    return 3 * x ** 2 - 2 * x + 5
```


## Regular Expressions (Regex)

Available on Python as **re** library, this function is special character sequence that specifies a search pattern and helps matching or finding other strings or sets of strings. 

re.findall() -  finds all the words that match the pattern passed on it and stores it in the list.
re.compile()

\w  represents “any word character” - alphanumeric (letters or numbers)
\W	Any Non-alphanumeric character
$	Matches the end of the line
\s	Matches whitespace
\S	Matches any non-whitespace character
*	Repeats a character zero or more times
*?	Repeats a character zero or more times (non-greedy)
+	Repeats a character one or more times
+?	Repeats a character one or more times (non-greedy)
[aeiou]	Matches a single character in the listed set
[^XYZ]	Matches a single character not in the listed set
[a-z0-9]	The set of characters can include a range
(	Indicates where string extraction is to start
)	Indicates where string extraction is to end
(.*)	Capture all
(abc|def)	Matches abc or def
abc…	Letters		
{m}	m Repetitions
123…	Digits		
{m,n}	m to n Repetitions
\d	Any Digit		
\D	Any Non-digit character		
.	Any Character		
?	Optional character
\.	Period		
[abc]	Only a, b, or c		
[^abc]	Not a, b, nor c		
^…$	Starts and ends
[a-z]	Characters a to z		
(…)	Capture Group
[0-9]	Numbers 0 to 9		
(a(bc))	Capture Sub-group


# Excercise and solutions

Final game end of the week

Crea un gioco per indovinare un numero creato in modalità Random con un massimo di 3 tentativi. Per eseguire questo gioco devo prima importare una libreria per la creazione Random del numero.
Inserimento nome user (input)
Inserimento numero (input)
```python
import random

a = random.randint(1,10)
name = input("Import name: ")
for x in range(3):
  user = int(input("Choose a number: "))
  if user == a:
    print("You won")
    break
  else:
    if x < 2:
      print("Sorry, you were not lucky, try again")
    else:
      print ("Sorry, it wasn't your day")
```

Q1. Chocolate firm chocoBury wants to do smart advertisement for their newly launched chocolate brand across Germany in 2019 and target right aged customers. They have collected the years of birth of all of the customers and want to calculate their respective age.

Given below is a list of 10 customers with year of birth, however, the list can be as large as several thousands of customers.

[1999, 1995, 2005, 2010, 2007, 2006, 1994, 1996, 1979, 2008]

The task is to write a function that returns the age of customers.
```python
customers = [1999, 1995, 2005, 2010, 2007, 2006, 1994, 1996, 1979, 2008]
age = [2020 - x for x in customers]
print (age)

[21, 25, 15, 10, 13, 14, 26, 24, 41, 12]

```

Q2. It costs much for the chocolate firm chocoBury to do marketing for wide range of customers. To save money, they want to narrow down the range of ages obtained in previous list.
    
Also, the oldest person and youngest person do not truly represent the targeted group for marketing campaign and they can be considered as outliers.


The task is to write a function that removes the outliers (the oldest and youngest person’s age) and return the new list with age of 8 persons (in this case which contains data for 10 customers initially).
    
Sample input: [20, 24, 14, 9, 12, 13, 25, 23, 40, 11]
Sample output: [20, 24, 14, 12, 13, 25, 23, 11]

```python
age = [21, 25, 15, 10, 13, 14, 26, 24, 41, 12]
age.remove(max(age))
age.remove(min(age))
print(age)

[21, 25, 15, 13, 14, 26, 24, 12]
```
Q3. The chocolate firm chocoBury did the survey of customers in Berlin and Munich separately and came up with the following lists of age of customers.

berlin = [15, 13, 16, 18, 19, 18, 10, 12 ]
munich = [7, 13, 15, 20, 19, 18, 10, 16]

However, marketing manager Henry thinks that a single list would be better to look at rather than having different lists from these 2 cities. So, Henry wants to have a common list from these 2 cities.

The task is to write a function that takes these 2 lists as input and return the common age values.

Sample input: [15, 13, 16, 18, 19, 15,9, 10], [13, 15, 20, 19, 17, 10, 16, 15]

Sample output: [15,13,16,18,19,15,10]
```python
berlin = [15, 13, 16, 18, 19, 18, 10, 12 ]
munich = [7, 13, 15, 20, 19, 18, 10, 16]
for x in berlin:
  if x in munich:
    print(x)

15
13
16
18
19
18
10
```
Q4. After careful investigation of the common age list, Henry, the marketing manager of the chocolate firm chocoBury, found out that many of the customer ages are simply duplicate values.  So, he asked Mark, the only software developer in the Chocolate company chocoBury, to give him the list with no redundant age values.

The task is to write a function that takes the list with duplicate values as input and return the list with unique age values. 

Sample input: [15,13,16,18,19,15,10]
Sample output: [15,13,16,18,19,10]

```python
comuni = [15, 13, 16, 18, 19, 18, 10]
set(comuni)
{10, 13, 15, 16, 18, 19}
```
Q5. Henry generally asks software developer Mark if a certain age value is present in the list of customer ages or not. However, Henry, a busy manager, often forgets what Mark replies and asks the same question sometimes multiple times.

Mark, a smart guy, thinks it is too boring for him and hence, he thinks why not he creates a function which will listen to Henry’s query and read through the age list & finally reply back to Henry if that age is present or not in the list.
   
The task is to write a function that takes an input list and value of age to find as input and return true or false if the age value is present or not.
            
Sample input: [15,13,16,18,19,15,10], 15
Sample output: True

Sample input: [15,13,16,18,19,15,10], 28
Sample output: False
```python
unici = [10, 13, 15, 16, 18, 10]
x = input("insert your number: ")
if int(x) in unici:
  print("True")
else:
  print("False")
insert your number: 13
True
```

## Intermediate (with function use)
1. You are given an array (which will have a length of at least 3, but could be very large) containing integers. The array is either entirely comprised of odd integers or entirely comprised of even integers except for a single integer N.

Write a method that takes the array as an argument and returns this “outlier” N.

Sample test cases:
[2, 4, 0, 100, 4, 11, 2602, 36]
Should return: 11 (the only odd number)

[160, 3, 1719, 19, 11, 13, -21]
Should return: 160 (the only even number)

find_outlier([2, 4, 6, 8, 10, 3])
Should return: 3
```python
def odd_even(a):

  odd_list = []
  even_list = []
  for x in a:
    if x % 2 ==1:
      odd_list.append(x)
    else:
      even_list.append(x)

  if len(odd_list)>len(even_list):
    return (even_list)
  else:
    return (odd_list)
    
a = [2, 4, 0, 100, 4, 11, 2602, 36]
b = [160, 3, 1719, 19, 11, 13, -21]
c = [2, 4, 6, 8, 10, 3]
p = odd_even(a)
p
[11]
p = odd_even(b)
p
[160]
p = odd_even(c)
p
[3]
```

2.  Your goal in this task is to implement a difference function, which subtracts one list from another and returns the result.

It should remove all values from list a, which are present in list b.

Lets call the function array_diff ( a , b )

Sample test cases:
array_diff([1,2],[1]) will return [2]
array_diff([1,2,2], [2]) will return [1]
```python
def array_diff (a,b):
  new_list = []
  for x in a:
    if x not in b:
      new_list.append(x)
      return new_list
      
a = [1,2]
b = [1]
array_diff (a,b)
[2]

a = [1,2,2]
b = [2]
array_diff (a,b)
[1]
```


# How to create a Github Readme File  

* Table of contents - https://www.setcorrect.com/portfolio/work11/  
* Markdown Cheatsheet - https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet  
                      - https://guides.github.com/features/mastering-markdown/
* Adding images - ![alt text](link of image)     
* Organizing with table - https://docs.github.com/en/github/writing-on-github/organizing-information-with-tables
    
