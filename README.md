# 42-Pool-Learning-Summary

Certainly! Here's a detailed breakdown of the concepts you need to learn for each project during the 42 pool competition:

### Shell (2 jours) :

Shell scripting involves automating tasks and managing files in Unix-like operating systems:

- **Commands**: Learn essential commands like `cd`, `ls`, `mv`, `cp`, and `rm` for navigating directories, listing files, moving/copying files, and removing files/directories.

### C (28 jours) :

1. **Pointers**:
   - **Project**: `C00`, `C01`, `C02`, `C03`
   - **Example**:
     ```c
     int *ptr; // Declaration of a pointer
     *ptr = 10; // Dereferencing a pointer
     ```

2. **Strings**:
   - **Project**: `C00`, `C01`, `C02`, `C03`, `C04`, `C05`, `C06`, `C07`, `C08`
   - **Example**:
     ```c
     char str[20]; // Declaration of a string
     strcpy(str, "Hello"); // String copy
     ```

3. **Arrays**:
   - **Project**: `C00`, `C01`, `C02`, `C03`, `C04`, `C05`, `C06`, `C07`, `C08`, `C09`, `C10`
   - **Example**:
     ```c
     int arr[5]; // Declaration of an array
     arr[0] = 10; // Accessing array elements
     ```

4. **Structures**:
   - **Project**: `C00`, `C01`, `C02`, `C03`, `C04`, `C05`, `C06`, `C07`, `C08`, `C09`, `C10`, `C11`, `C12`
   - **Example**:
     ```c
     struct Person {
         char name[50];
         int age;
     };
     ```

5. **Functions**:
   - **Project**: `C00`, `C01`, `C02`, `C03`, `C04`, `C05`, `C06`, `C07`, `C08`, `C09`, `C10`, `C11`, `C12`
   - **Example**:
     ```c
     int add(int a, int b) {
         return a + b;
     }
     ```

6. **Input/Output**:
   - **Project**: `C00`, `C01`, `C02`, `C03`, `C04`, `C05`, `C06`, `C07`, `C08`, `C09`, `C10`, `C11`, `C12`, `C13`
   - **Example**:
     ```c
     printf("Enter a number: ");
     scanf("%d", &num);
     ```

7. **Makefile**:
   - **Project**: `C06`, `C07`, `C08`, `C09`, `C10`, `C11`, `C12`, `C13`
   - **Example**:
     ```make
     all: myprogram

     myprogram: main.c
         gcc -o myprogram main.c
     ```

8. **Compilation**:
   - **Project**: All C projects (`C00` to `C13`)
   - **Example**:
     ```bash
     gcc -o myprogram main.c
     ```

9. **Compilation Flags**:
   - **Project**: All C projects (`C00` to `C13`)
   - **Example**:
     ```bash
     gcc -Wall -Wextra -Werror -o myprogram main.c
     ```


### Apply Concepts:

Certainly! Here's a detailed step-by-step guide on how to apply each concept with code examples for each project during the 42 pool competition:

### 1. Pointers

**Concept**: Pointers in C are variables that store memory addresses, crucial for dynamic memory allocation and efficient data manipulation.

**Example**:

```c
// Project: C00
// Example: Using pointers to manipulate integers

#include <stdio.h>

int main() {
    int num = 10;
    int *ptr = &num; // Declare and initialize pointer

    printf("Value of num: %d\n", num); // Output: 10
    printf("Address of num: %p\n", &num); // Output: Address of num
    printf("Value of num using pointer: %d\n", *ptr); // Output: 10

    *ptr = 20; // Modify value through pointer
    printf("Modified value of num: %d\n", num); // Output: 20

    return 0;
}
```

### 2. Strings

**Concept**: Strings in C are arrays of characters terminated by a null character (`\0`), used extensively for text manipulation.

**Example**:

```c
// Project: C03
// Example: Concatenating strings

#include <stdio.h>
#include <string.h>

int main() {
    char str1[20] = "Hello";
    char str2[20] = " World";

    strcat(str1, str2); // Concatenate str2 to str1
    printf("Concatenated string: %s\n", str1); // Output: Hello World

    return 0;
}
```

### 3. Arrays

**Concept**: Arrays in C store multiple elements of the same data type in contiguous memory locations, accessed using indices.

**Example**:

```c
// Project: C01
// Example: Sum of elements in an array

#include <stdio.h>

int main() {
    int arr[5] = {1, 2, 3, 4, 5};
    int sum = 0;

    for (int i = 0; i < 5; i++) {
        sum += arr[i];
    }

    printf("Sum of array elements: %d\n", sum); // Output: 15

    return 0;
}
```

### 4. Structures

**Concept**: Structures in C allow you to create custom data types by grouping variables of different data types under a single name.

**Example**:

```c
// Project: C02
// Example: Using structures to store and display information

#include <stdio.h>

struct Person {
    char name[50];
    int age;
};

int main() {
    struct Person person1;

    strcpy(person1.name, "John");
    person1.age = 30;

    printf("Person's name: %s\n", person1.name); // Output: John
    printf("Person's age: %d\n", person1.age); // Output: 30

    return 0;
}
```

### 5. Functions

**Concept**: Functions in C are blocks of code that perform a specific task, promoting code reuse and modular programming.

**Example**:

```c
// Project: C04
// Example: Function to calculate factorial

#include <stdio.h>

int factorial(int n) {
    if (n == 0 || n == 1)
        return 1;
    else
        return n * factorial(n - 1);
}

int main() {
    int num = 5;
    int fact = factorial(num);

    printf("Factorial of %d: %d\n", num, fact); // Output: 120

    return 0;
}
```

### 6. Input/Output

**Concept**: Input/Output operations in C involve functions like `printf` for formatted output and `scanf` for formatted input.

**Example**:

```c
// Project: C05
// Example: Reading and printing user input

#include <stdio.h>

int main() {
    int num;

    printf("Enter a number: ");
    scanf("%d", &num);

    printf("You entered: %d\n", num);

    return 0;
}
```

### 7. Makefile

**Concept**: A Makefile automates the building and compiling of programs, specifying dependencies and compilation commands.

**Example**:

```make
# Project: C06
# Example: Makefile for compiling a C program

all: myprogram

myprogram: main.c
    gcc -o myprogram main.c

clean:
    rm -f myprogram
```

### 8. Compilation

**Concept**: Compilation in C translates source code into machine code using a compiler like GCC.

**Example**:

```bash
# Project: C07
# Example: Compiling a C program using GCC

gcc -o myprogram main.c
```

### 9. Compilation Flags

**Concept**: Compilation flags in C, like `-Wall`, `-Wextra`, and `-Werror`, enable warnings and treat them as errors to ensure code quality.

**Example**:

```bash
# Project: C08
# Example: Compiling with flags to enable warnings as errors

gcc -Wall -Wextra -Werror -o myprogram main.c
```

