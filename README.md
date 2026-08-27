# ECE2112_PA1
Milan, Rye Keane Lorenzo | 2ECE-D

# Problem 1: Word Rotation Problem
Create a function that accepts a non-empty string. Move the first character of the string to the end while keeping all remaining characters in their original order. Preserve the capitalization of every character.

The `rotate_word` function solves this problem by taking advantage of slicing in Python. Instead of using a loop to deal with moving the letters one by one, every letter starting from the second character until the end can be grabbed instead. 

```
text[1:]
```

Because Python strings can't be changed in place, taking out the first letter using index proved to be an effective operation that does not produce any changes with the original word.

```
text[0]
```

Using the addition operator, allows for the picked off first character to be placed right back on the end of the sliced string. This produces a rotated word in one line. 

```
return text[1:] + text[0]
```

# Problem 2: Username Builder
Create a function that accepts two strings, first_name and last_name, converts all letters to lowercase, removes all spaces from both the first and last names, and joins the processed names using a single period.

# Problem 3: Bookend Swap Problem
Create a function that accepts a list containing at least two elements and unpacks it into three variables—first for the first element, middle for a list containing everything between the first and last elements, and last for the last element—to return a new list without modifying the input list, in which the first and last elements have exchanged positions and the elements in middle remain in their original order.
