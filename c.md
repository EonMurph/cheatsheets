# C Cheat Sheet

- [C Cheat Sheet](#c-cheat-sheet)
  - [General](#general)
  - [Variables](#variables)
  - [Basic Function Calls](#basic-function-calls)
    - [`printf(string, placeholders)`](#printfstring-placeholders)
      - [Format Codes for Printing](#format-codes-for-printing)
  - [Conditionals](#conditionals)
    - [Logical Operations](#logical-operations)
  - [Loops](#loops)
    - [While Loops](#while-loops)
  - [Error Messages](#error-messages)

## General

- All function calls must end with a semi-colon.
- The `#include` line at the start of your files
  tells the compiler to essentially import these "header files",
  basically libraries from Python.
  - A list of frequently used functions and their "header files" can be found [here](https://manual.cs50.io/).
- All strings must be encased in `"`; whereas single characters are encased in `'`.
- A comment is denoted by `// your comment`

## Variables

- All variables must start with a datatype.
  - The common types are the following:
    - `char` - A single character
      <sub><sup>(P.S a string can be defined as such: `char greeting[] = "Hello World!"`)</sup></sub>
    - `int` - Whole numbers, both positive and negative
    - `float` - Floating-point numbers
    - `double` - Similar to `float` but occupies more storage space
      allowing for greater accuracy of decimals
    - `void` - Absence of type,
      used most often for functions that return no value

## Basic Function Calls

### `printf(string, placeholders)`

- this function is the equivalent of `print()` from Python.
- To give a variable into the string, use `%s`
  and then follow the string with the variable within the function call

#### Format Codes for Printing

- `%c` for `char`
- `%s` for strings
- `%i` for `int`
- `%f` for `float`
- `%lf` for `double`

## Conditionals

- Single conditional:

  ```C
  if (x)
  {

  }
  ```

- Double conditional:

  ```C
  if (x)
  {

  }
  else
  {

  }
  ```

  - n<sup>th</sup> tuple conditional:

  ```C
  if (x)
  {

  }
  else if (y)
  {

  }
  else
  {

  }
  ```

### Logical Operations

- OR can be accessed using `||`.
- AND can be accessed using `&&`.

## Loops

### While Loops

The syntax is as follows:

```C
while (conditional)
{
  // code to execute
}
```

## Error Messages

The first line of the error tells you:

- Where the error occurred, and
- What the error is.
- An example is:
  `hello.c:5:5`
  <br>this is saying the error occurred in the file `hello.c`, on line 5 at character 5
