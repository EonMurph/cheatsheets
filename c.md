# C Cheat Sheet

- [C Cheat Sheet](#c-cheat-sheet)
  - [General](#general)
    - [Arithmetic Operators](#arithmetic-operators)
  - [Variables](#variables)
    - [Type Casting](#type-casting)
  - [Basic Function Calls](#basic-function-calls)
    - [`printf(string, placeholders)`](#printfstring-placeholders)
      - [Format Codes for Printing](#format-codes-for-printing)
  - [Conditionals](#conditionals)
    - [Logical Operations](#logical-operations)
  - [Loops](#loops)
    - [While Loops](#while-loops)
    - [For Loops](#for-loops)
  - [Functions](#functions)
    - [Function Syntax](#function-syntax)
    - [Function Prototypes](#function-prototypes)
  - [Error Messages](#error-messages)

## General

- All function calls must end with a semi-colon.
- The `#include` line at the start of your files
  tells the compiler to essentially import these "header files",
  basically libraries from Python.
  - A list of frequently used functions and their "header files" can be found [here](https://manual.cs50.io/).
- All strings must be encased in `"`; whereas single characters are encased in `'`.
- A comment is denoted by `// your comment`

### Arithmetic Operators

- `+` - addition
- `-` - subtraction
- `*` - multiplication
- `/` - division
- `%` - modulo (get the remainder after division)

## Variables

- All variables must start with a datatype.
  - The common types are the following:
    - `char` (1 byte) - A single character
      <sub><sup>(P.S a string can be defined as such: `char greeting[] = "Hello World!"`)</sup></sub><br><br>

    - `int` (2/4 bytes) - Whole numbers, both positive and negative
    - `long` (4/8 bytes) - Increase the range of `int`

    - `float` (4 bytes) - Floating-point numbers
    - `double` (8 bytes) - Similar to `float` but occupies more storage space
      allowing for greater accuracy of decimals<br><br>

    - `void` - Absence of type,
      used most often for functions that return no value
- You can turn a variable into a constant by using the keyword `const`:
  - `const int n = 3`

### Type Casting

You can cast a variable of one type to another by placing the desired data type in front of the variable name,
with the data type surrounded by `()`.

- Example:

  ```C
  int x = 1;
  int y = 3;

  printf("%i", x / y); // Output: 0
  printf("%f", (float)x, (float)y); // Output: 0.333...
  ```

## Basic Function Calls

### `printf(string, placeholders)`

- this function is the equivalent of `print()` from Python.
- To give a variable into the string, use `%s`
  and then follow the string with the variable within the function call

#### Format Codes for Printing

- `%c` for `char`
- `%s` for strings
- `%i` for `int`
- `%li` for `long`

- `%f` for `float` or `double`
- `%lf` for `double`
  - for floats you can add a `.n` before the `f` or `lf`, where `n` is the number of decimal points you want.

## Conditionals

- Single conditional:

  ```C
  if (x)
  {
      // code to be executed
  }
  ```

- Double conditional:

  ```C
  if (x)
  {
      // code to be executed
  }
  else
  {
      // code to be executed
  }
  ```

  - n<sup>th</sup> tuple conditional:

  ```C
  if (x)
  {
      // code to be executed
  }
  else if (y)
  {
      // code to be executed
  }
  else
  {
      // code to be executed
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
    // code to be executed
}
```

- Example:

  ```C
  int i = 3;
  while (i > 0)
  {
    printf(i);
  }
  ```

- You can create a forever loop with the following:

  ```C
  while (true)
  {
      // code to be executed
  }
  ```

### For Loops

```C
for (define variable; conditional; increment/decrement variable)
{
    // code to be executed
}
```

- Example:

  ```C
  for (int i = 0; i < 3; i++)
  {
      printf(i);
  }
  ```

## Functions

### Function Syntax

```C
returnType functionName(parameters)
{
    // code to be executed
}
```

- Example:

  ```C
  void meow(void)
  {
    printf("meow\n");
  }
  ```

To return a value just use the `return` keyword,
e.g.

```C
int add(int a, int b)
{
    return a + b;
}
```

### Function Prototypes

Functions must be defined before they are called.
But the code they will execute does not have to be in that definition.
These statements are known as function prototypes.

You must have the same function name, return type and parameter names.<br>
This allows you to keep the `main` function at the top of the file, which is preferable.

- Example:

  ```C
  void meow(int n);

  int main(void){
      // main code
  }

  void meow(int n)
  {
      // meow code
  }
  ```

## Error Messages

The first line of the error tells you:

- Where the error occurred, and
- What the error is.
- An example is:
  `hello.c:5:5`
  <br>this is saying the error occurred in the file `hello.c`, on line 5 at character 5
