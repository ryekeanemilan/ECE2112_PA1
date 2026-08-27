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

The `make_username` function creates the final username by applying operations one right after the other. Going from left to right, we first make all the letters into lowercase.

```
.lower()
```
Because the first step returns a string, it is possible to immediately follow up with `.replace()` because it hunts down and removes all the spaces found in the text. This is particularly useful in collapsing multi-word inputs such as "De Leon".

```
.replace(" ", "")
```

The same process is applied to both the first and last names, and to polish it further, a period string is added between them to join the final username together.

```
return first_name.lower().replace(" ", "") + "." + last_name.lower().replace(" ", "")
```

# Problem 3: Bookend Swap Problem
Create a function that accepts a list containing at least two elements and unpacks it into three variables—first for the first element, middle for a list containing everything between the first and last elements, and last for the last element—to return a new list without modifying the input list, in which the first and last elements have exchanged positions and the elements in middle remain in their original order.

The `swap_bookend` function uses Python's extended sequence unpacking to separate the list into the parts needed. With this approach, Python automatically decides that the first item falls under the `first` variable, the last item under `last,` and immediately groups everything into the `middle` variable.

```
first, *middle, last = items
```

To obtain the final part of the solution, a new list is created in which `last` sits at the front and `first` at the back. The asterisk is needed one more time so the middle items sit properly between the swapped ends without extra brackets showing up. 

```
return [last, *middle, first]
```
