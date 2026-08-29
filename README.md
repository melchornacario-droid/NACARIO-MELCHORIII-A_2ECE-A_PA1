## Problem 1 (Word Rotation Problem)
Create a function that interchanges the first and last character in a string. Keep the capitalizations.

The following functions and methods were used in this problem:

* `text[1:]` - a built in function that extracts all the characters from 2nd to the end of the string

Example: `text="Craig"` `text[1:]` --> `['r','a','i','g']`

* `text[0]` - A function to retrieve the first character in a string
  
Example: `text[0]` --> `("C")`

These functions were used to create a function that switches the first and last character of a string

```python
def rotate_word(text):
    new_word=text[1:] + text[0]
    return new_word
print(rotate_word("python")) 
print(rotate_word("logic")) 
print(rotate_word("Code")) 
print(rotate_word("A"))
```
## Problem 2 (USERNAME BUILDER PROBLEM)

Create a function that accepts two non-empty strings, converts all letters to lowercase, removes all spaces and joins them using one period.

The following functions and methods were used in this problem:
* `.lower()` - turns the case of the string into lowercase

Example: `a = "ABC"` --> `a.lower()` --> `"abc"`

* `.replace()` - A function that replaces an existing character inside of a string with a new character. `replace("Old", "New")`, the first parameter is the old character while the second parameter is the new character.

Example: `a = "ABC"` --> `a.replace("C", "D")` --> `"ABD"`

* `"".join()` - A method to join the elements of an iterable(list) into a single string.
Example: `"".join(['C','r','a','i','g'])` --> `("Craig")`

These functions were used to create a function that creates a username from the strings typed by the user with the characteristics of:
* Lowercase
* No spaces
* A period between the first and last name

```python
def make_username(first_name, last_name):
    n = first_name.lower().replace(" ", "")
    m = last_name.lower().replace(" ", "")
    user = [n, m]
    return ".".join(user)
print(make_username("Ada", "Lovelace"))     
print(make_username("Alan", "Turing"))        
print(make_username("Ana Maria", "De Leon"))
```

## Problem 3 (BOOKEND SWAP PROBLEM)

Create a function that unpacks a list into its first, last, and middle elements and switches the position of the first and last element.

The following functions and methods were used in this problem:
* `Extended Sequence Unpacking`: Unpacks the first element into first, the last element into last, and all elements between them into the list variable middle using the asterisk operator.

  Example: `a = ['apple","banana"]` --> `first, *middle, last = a` --> `first="apple", middle=[], last="banana"`

This function was used in creating a function that switches the first and last element of a list:

```python
def swap_bookends(items):
    first, *middle, last = items
    return [last, *middle, first]
print(swap_bookends([1, 2, 3, 4, 5, 6]))  
print(swap_bookends(["red", "green", "blue"])) 
print(swap_bookends([8, 3]))
```
