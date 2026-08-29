## Problem 1 (Word Rotation Problem)
Create a function that interchanges the first and last character in a string. Keep the capitalizations.

The following functions and methods were used in this problem:

* `list()` - a built in function that converts a string into a list

Example: `list("Craig")` --> `['C','r','a','i','g']`

* `"".join()` - A method to join the elements of an iterable(list) into a single string.
  
Example: `"".join(['C','r','a','i','g'])` --> `("Craig")`

These functions were used to create a function that switches the first and last character of a string

```python
def rotated_word(text):
    n = list(text)
    n[0], n[-1] = n[-1], n[0]
    return "".join(n)

print(rotated_word(input("Enter word: ")))```
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
```

## Problem 3 (BOOKEND SWAP PROBLEM)

Create a function that unpacks a list into its first, last, and middle elements and switches the position of the first and last element.

The following functions and methods were used in this problem:
* `.split()`: A string method called on the result of `input()` to break the string into a list of separate items based on spaces.

  Example: `a = "ABC"` --> `a.split()` --> `['A','B','C']`

This function was used in creating a function that switches the first and last element of a list:

```python
def swap_bookends(lst):
    first = lst[0]
    second = lst[1:-1]
    third = lst[-1]
    swap = [third] + second + [first]
    return swap

print(swap_bookends(input("Enter Items Separated by Spaces: ").split()))
x = input("First Name: ")
y = input("Last Name: ")
print(make_username(x, y))
