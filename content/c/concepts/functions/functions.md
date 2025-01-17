---
Title: 'Functions'
Description: 'Functions are blocks of code that can be run multiple times within a program. They are stored under a name similar to a variable and can be called using this name. A function is declared with the return type, the function name, parameter(s), and the code for it to run in curly brackets. pseudo return_type name(parameters) { // Code goes here } '
Subjects:
  - 'Code Foundations'
  - 'Computer Science'
Tags:
  - 'Functions'
  - 'Arguments'
CatalogContent:
  - 'learn-c'
  - 'paths/computer-science'
---

Functions are blocks of code that can be run multiple times within a program. They are stored under a name similar to a variable and can be called using this name.

## Declaring a Function

A function is declared with the return type, the function name, parameter(s), and the code for it to run in curly brackets.

```pseudo
return_type name(parameters) {
  // Code goes here
}
```

A function named `greet()` that prints a greeting to the console can be declared like this:

```c
void greet(void) {
  puts("Howdy!");
}
```

## Calling a Function

After a function is declared, it can be called in the program. The syntax for this is the variables name followed by parenthesis.

```c
#include <stdio.h>

// Declaring the function

void greet(void) {
  puts("Howdy!");
}

// Calling the function inside main()

int main() {
  greet();
}
```

The output would be:

```shell
Howdy!
```

## Arguments

The values passed to a function are known as arguments. They represent the actual input values that can be used within the function.

```c
#include <stdio.h>

void max(int x, int y) {
  if (x > y)
    printf("%d is the bigger number\n", x);
  else
    printf("%d is the bigger number\n", y);
}

int main() {
  int a = 20;
  int b = 30;

  max(a, b);

  return 0;
}
```

Here's another example:

```c
#include <stdio.h>

void greet(char* name) {
  printf("Howdy %s!\n")
}

int main() {
  greet("John Doe"); // Output: Howdy John Doe!
  return 0;
}
```

## Returning Values

A function is also capable of returning a value back to were it was called using the `return` keyword. This is useful for computing values within a function. Notice that the word proceeding the function name indicates the type of value returned.

```c
#include <stdio.h>

int add(int a, int b) {
  return a + b;
}

int main(void) {
  int num = add(1, 1);
  printf("%d\n", num);
}
```

Here, the `add()` function has a return value of `int`.
