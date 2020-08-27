# Lecture 2

## Objectives:
Discuss and demonstrate:
- The concept of data types
- variables, assignments
- numerical types
- arithmetic operators and expressions
- comments in the program
- understanding error messages

## Arithmetic Operators
There are many operators that can be used to get a mathematical result.

| Operator    | Description | Notes |
| --- | --- | --- |
| + | addition | |
| - | subtraction | |
| * | multiplication| |
| / | division (float) | 5 / 2 -> 2.5 |
| // | division (floor) | 5 // 2 -> 2 |
| % | modulus | 5 % 2 -> 1 |
| ** | exponent | 2 ** 5 -> 32 |

## Data Types
There are many different data types in python. You can always test what python a data type is using the following function:
```
>>> x = 5
>>> type(x)
<class 'int'>
```
### Integers
Integers are whole numbers without decimal values. In many languages, there is a "biggest" value that an integer can be.  
In Python 3, there is effectively no limit to how long an integer value can be. Of course, it is constrained by the amount of memory your system has but beyond that you can represent a very large number.

### Floating-Point Numbers
The float type in Python designates a floating-point number. float values are specified with a decimal point. Optionally, the character e or E followed by a positive or negative integer may be appended to specify scientific notation:

```
>>> x = 5.2
>>> type(x)
<class 'float'>
```
### Characters
Single letters are called characters or char.
Characters align to the [ASCII standard](http://www.asciitable.com/) where every letter has a unique number.
- 'a'
- 'A'

These are examples of Characters, you can also convert a character from the letter representation to the numerical representation"
```
>>> ord('a')
97
>>> ord('A')
65
```
This conversion can go the other way too.
```
>>> chr(65)
A
>>> chr(66)
B
```

#### Special Characters
To represent keyboard actions that are difficult to type, several special characters are used. Here are a few common special characters.

|Character| Meaning|
|---|---|
| \n | New Line (Enter) |
| \t | Tab |
| \\" | Displays a quote |
| \\\ | Displays a backslash |

### Strings
Strings are one or more characters in a row, we show the beginning and end of a string by using quotations.
Strings can be denoted in several methods:
 - "I am a string"
 - 'I am also a string'
 - '''This is also a string'''  

The key is to have the same beginning and ending quotation to show the matched pair.
We will usually use double quotes("") for strings since that is the standard in other programming languages.

### Boolean
Boolean types have two possible states:
- True
- False

We use booleans to make decisions or evaluate a criteria. Anything that can be answered as a yes or no can be stored as a boolean value.

### Converting types
Often when we get input, we accept whatever they type as a string. If the value they gave us was actually a number, we will have to convert the data type to do mathematical manipulation.
```
>>> x = "5"
>>> y = x + 10
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
```

To avoid this error we must first convert one of the data types to match. In this case, we want to convert the string "5" to the integer 5.
```
>>> x = "5"
>>> y = int(x) + 10
>>> print(y)
15
```

You cannot convert a string to a number if the letters of the string are not actually numbers. You will get an error.
```
>>> int("Hello")
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: invalid literal for int() with base 10: 'Hello'
```

### Combining Types - Numbers
Datatypes can sometimes be combined without a type change involved. If we do this, what would the resulting type be?
```
>>> x = 5
>>> y = 7.2
>>> z = x + y
>>> print(z)
12.2
>>> type(z)
<class 'float'>
```
Here we can see that an integer and a floating-point number are added. The result is a float. If we had converted the result to an integer, data would have been lost. An integer cannot hold the decimal portion of the floating-point number and that data would have been dropped.

Sometimes, it is okay to lose the decimal portion of a floating point number.
```
>>> x = 7.2
>>> y = int(x)
>>> print(y)
7
```

Note: the decimal portion is not rounded, it is just dropped.
```
>>> print( int(8.8) )
8
```

### Combining Types - Letters
Two strings can be joined with the + operator.
```
>>> print("Hello " + "world")
Hello world
```

We can also join a string and a character with the same method.
```
>>> print("Hello " + '!')
Hello!
```

You cannot join a number with a string, you will get an error.
```
>>> print("Hello" + 1)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
```

If you want to do this, you can convert the number to become a string.
This works with both literal numbers and with variables that are numbers. It also works with both integers and floating-point numbers.
```
>>> print("Hello" + str(1))
Hello1
>>> x = 5
>>> print("Hello" + str(x))
Hello5
>>> y = 2.8
>>> print("Hello" + str(y))
Hello2.8
```
### Quiz
1. What is the ord (ASCII) value of capital 'G'?

2. You're trying to determine how many cars you need to transport a number of people. Which of the following would give you the number of cars needed? We are assuming every car can hold 4 people.
  - cars = people / 4
  - cars = people % 4
  - cars = people ** 4
  - cars = people // 4

3. What is the output type of the following code?
```
>>> approxPi = 22/7
>>> type(approxPi)
```
	- <class 'float'>
	- <class 'int'>
	- <class 'str'>
	- <class 'chr'>

4. What would be the result of the following code?
```
print("Hello\nworld\tHave a nice\n \"Day\"")
```

  - It will produce an error
  - Hello world Have a nice "Day"
  - Hello
    world   Have a nice
     "Day"
  - Hello\nworld\tHave a nice\n \"Day\"

5. Boolean variables only have two possible states:
  - True
  - False
