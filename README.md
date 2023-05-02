# Code Zero To Hero Curriculum

## Python

### Variables

- Creating Variables
- Casting
  - You can specify the data type of a variable
  - `str()`, `int()`, `float()`
- Get the Type
  - You can get the data type of a variable with the `type()` function

### Naming

- Snake Case
  - `my_name = 'Christine`
- Pascal Case
  - `MyName = 'Christine'`
- Assigning Multiple Values
  - You can assign values to multiple variables in one line
    - `x, y, z = 'Orange', 'Banana', 'Cherry'`
  - You can assign the same value to multiple variables in one line
    - `x = y = z = 'Orange`
    - If you have a collection of values in a list, tuple etc. Python allows you to extract the values into variables. This is called _unpacking_
      ```
      fruits = ['apple', 'banana', 'cherry']
      x, y, z = fruits
      ```

### Output

- `print()` function is often used to output variables
  ```
  x = 'Python is cool.'
  print(x)
  ```

### Data Types

- Built-in Data Types
  - Text type: `str`
  - Numeric types: `int`, `float`
  - Sequence types: `list`, `tuple`, `range`
  - Mapping type: `dict`
  - Set type: `set`
  - Boolean type: `bool`
  - Binary types: `bytes`, `bytearray`
  - None type: `NoneType`
- You can _cast_ to change data types
  ```
  x = 100
  print(x)        # Output: 100
  print(str(x))   # Output: '100'
  ```

#### Strings

- Multiline strings, three single or double quotes
- Strings are lists/arrays of characters
- Since strings are arrays, we can loop through the characters in a string, with a `for` loop
- To get the length of a string, use the `len()` function
- To check if a certain phrase or character is present in a string, we can use the keyword `in`

  ```
  txt = 'The best things in life are free!'
  print('free' in txt)

  # If statement
  if 'free' in txt:
      print('Yes, 'free' is present.')
  ```

- To check if a certain phrase or character is NOT present in a string, we can use the keyword `not in`

  ```
  txt = 'The best things in life are free!'
  print('expensive' not in txt)

  # If statement
  if 'expensive' not in txt:
      print('No, 'expensive' is NOT present.')
  ```

- Slicing
  - Specify the start index and the end index, separated by a colon, to return a part of the string
    ```
    b = 'Hello, World!'
    print(b[2:5])
    ```
  - Slice from the start
    - By leaving out the start index, the range will start at the first character
      ```
      b = 'Hello, World!'
      print(b[:5])
      ```
  - Slice to the end
    - By leaving out the end index, the range will go to the end
      ```
      b = 'Hello, World!'
      print(b[2:])
      ```
  - Reversing (Negative index)
  - Step
- String Methods
  - `upper()`, `lower()`, `strip()`, `capitalize()`, `title()`, `join()`
- Contatenatation
  - To concatenate, or combine, two strings you can use the + operator
    ```
    a = 'Hello'
    b = 'World'
    c = a + ' ' + b
    print(c)
    ```
- Interpolation

  ```
  greeting = 'Hi'
  name = 'Justin'

  # Format method
  txt = '{}, {}'.format(greeting, name)

  # f-string
  txt = f'{greeting}, {name}'
  ```

### Boolean

- In programming you often need to know if an expression is True or False. You can evaluate any expression in Python, and get one of two answers, True or False. When you compare two values, the expression is evaluated and Python returns the Boolean answer
  ```
  print(10 > 9)
  print(10 == 9)
  print(10 < 9)
  ```

### Operators

- Arithmetic
  - `+, -, *, /, %, **, //`
- Assignment
  - `=`, `x = 5` is the same as `x = 5`
  - `+=`, `x += 3` is the same as `x = x + 3`
  - `-=`, `x -= 3` is the same as `x = x - 3`
- Comparison
  - `==, !=, >, <, >=, <=`
- Logical
  - `and, or, not`
- Identity
  - `is, is not`
- Membership
  - `in, not in`

### Lists

- `list()` contructor
  ```
  this_list = list(('apple', 'banana', 'cherry'))
  print(this_list)
  ```
- Access items

  ```
  a_list = ['apple', 'banana', 'cherry', 'orange', 'kiwi', 'melon', 'mango']

  # List items are indexed and you can access them by referring to the index number
  print(a_list[1]) # Output 'banana'

  # Negative indexing means start from the end
  print(a_list[-1]) # Output ['mango', 'melon', 'kiwi', ...]

  # You can specify a range of indexes by specifying where to start and where to end the range
  print(a_list[2:5]) # Output ['cherry', 'orange', 'kiwi']

  # By leaving out the start value, the range will start at the first item
  print(a_list[:4]) # Output ['apple', 'banana', 'cherry', 'orange']

  # By leaving out the end value, the range will go on to the end of the list
  print(a_list[2:]) # Output ['cherry', 'orange', 'kiwi', 'melon', 'mango']
  ```

- Check if item exists
  ```
  a_list = ['apple', 'banana', 'cherry']
  if 'apple' in a_list:
    print('Yes, 'apple' is in the fruits list')
  ```
- Change list items
  - To change the value of a specific item, refer to the index number
    ```
    a_list = ['apple', 'banana', 'cherry']
    a_list[1] = 'raspberry'
    print(a_list)
    ```
- Add list items

  ```
  a_list = ['apple', 'banana', 'cherry']

  # To add an item to the end of the list, use the `append()` method
  a_list.append('orange')
  print(a_list)

  # To insert a list item at a specified index, use the `insert()` method
  a_list.insert(1, 'orange')
  print(a_list)
  ```

- Remove list items

  ```
  a_list = ['apple', 'banana', 'cherry']

  # The `remove()` method removes the specified item
  a_list.remove('banana')
  print(a_list)

  # The `pop()` method removes the specified index
  a_list.pop(1)
  print(a_list)

  # If you do not specify the index, the `pop()` method removes the last item
  a_list.pop()
  print(a_list)

  # *Note `pop()` returns the value removed from list. So, you can assign the popped value to a variable
  x = a_list.pop()

  # The `del` keyword also removes the specified index
  del a_list[0]
  print(a_list)

  # The `clear()` method empties the list
  a_list.clear()
  print(a_list)
  ```

- Loop lists

  - You can loop through the list items by using a `for` loop

  ```
  this_list = ['apple', 'banana', 'cherry']
  for x in this_list:
    print(x)

  # While loop
  i = 0
  while i < len(this_list):
    print(this_list[i])
    i = i + 1
  ```

- List comprehension

  - Loop through list with one line of code

  ```
  fruits = ['apple', 'banana', 'cherry', 'kiwi', 'mango']

  new_list = [x for x in fruits if 'a' in x]

  print(new_list)
  ```

- Sort
  - Lists have a `sort()` method that will sort the list alphanumerically, ascending, by default
  ```
  this_list = ['orange', 'mango', 'kiwi', 'pineapple', 'banana']
  this_list.sort()
  print(this_list)
  ```
- Join
