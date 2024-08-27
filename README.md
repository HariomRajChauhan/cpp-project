# LIPI Documentation

Welcome to the language documentation! This guide will help you understand how to write and execute code in our language.

## Basic Syntax

### Program Structure

A program is a sequence of statements, each ending with a semicolon.

plaintext
statement1;
statement2;
...


## Statements

### Print Statement

Use bhana to print a value or expression to the output.

*Syntax:*
plaintext
bhana(expression);


*Examples:*
plaintext
bhana(5 + 3);  // Prints 8
bhana("Hello, World!");  // Prints Hello, World!


### Input Statement

Use suna to read a value from the user and store it in a variable.

*Syntax:*
plaintext
suna(variable_name);


*Examples:*
plaintext
suna(name);  // Reads input into the variable `name`


### Declaration Statement

Use this to declare a variable. You cannot initialize a variable at the time of declaration.

*Syntax:*
plaintext
type variable_name;


*Examples:*
plaintext
purna age;  // Declares an integer variable `age`
dasa salary;  // Declares a decimal variable `salary`


### Assignment Statement

Use this to assign a value to an existing variable.

*Syntax:*
plaintext
variable_name = expression;


*Examples:*
plaintext
age = 31;  // Assigns the value 31 to the variable `age`


### If Statement

Use yadi to execute a block of code conditionally. You can include an anyatha block for the else condition.

*Syntax:*
plaintext
yadi(expression) {
    // block of code
} anyatha {
    // else block of code
}


*Examples:*
plaintext
yadi(age > 18) {
    bhana("Adult");
} anyatha {
    bhana("Minor");
}


### While Statement

Use jabasamma to repeat a block of code while a condition is true.

*Syntax:*
plaintext
jabasamma(expression) {
    // block of code
}


*Examples:*
plaintext
jabasamma(age < 30) {
    age = age + 1;
}


### For Statement

Use lagi to loop through a range of values, specifying initialization, condition, and update.

*Syntax:*
plaintext
lagi(initialization; condition; update) {
    // block of code
}


*Examples:*
plaintext
lagi(i = 0; i < 10; i = i + 1) {
    bhana(i);
}


### Function Definition

Use kaam to define a new function.

*Syntax:*
plaintext
kaam return_type function_name(parameter_list) {
    // block of code
}


*Examples:*
plaintext
kaam purna add(purna a, purna b) {
    firta a + b;
}


### Return Statement

Use firta to return a value from a function.

*Syntax:*
plaintext
firta(expression);


*Examples:*
plaintext
firta result;


## Expressions

### Basic Expressions

You can perform operations with numbers, strings, and other values.

*Syntax:*
plaintext
term { ("+" | "-" | "*" | "/") term }


*Examples:*
plaintext
5 + 3 * 2
"Hello"
'c'


### Logical Expressions

Combine logical terms using &&, ||, or ! to form complex conditions.

*Syntax:*
plaintext
logical_term { ("&&" | "||" | "!") logical_term }


*Examples:*
plaintext
age > 18 && age < 65


### Comparison

Compare values using operators like ==, !=, <, <=, >, and >=.

*Syntax:*
plaintext
expression (== | != | < | <= | > | >=) expression


*Examples:*
plaintext
age == 30


### Modulo Expression

Calculate the remainder of a division using %.

*Syntax:*
plaintext
expression % expression


*Examples:*
plaintext
10 % 3  // Results in 1


## Data Types

- purna: Integer
- dasa: Decimal
- akshar: String
- paath: Character
- khali: Void

*Examples:*
plaintext
purna count;  // Declare an integer variable
dasa price;   // Declare a decimal variable
akshar name;  // Declare a string variable
paath initial;  // Declare a character variable


## Identifiers and Literals

- *Identifier:* A name for a variable or function, starting with a letter or underscore, followed by letters, numbers, or underscores (e.g., variable1, _temp).
- *Number:* An integer or decimal value (e.g., 42, 3.14).
- *String:* A sequence of characters enclosed in double quotes (e.g., "Sample text").
- *Character:* A single character enclosed in single quotes (e.g., 'A').

*Examples:*
plaintext
number = 42;
text = "Sample text";
letter = 'A';


For further assistance or examples, please refer to additional resources or community forums.

Happy coding!

---
=======
# Lipi

## Building the Project

### Prerequisites

- CMake 3.10 or higher
- A C++ compiler (e.g., g++, clang++)

### Steps

1. **Clone the Repository**:
    ```sh
    git clone https://github.com/yourusername/lipi.git
    cd lipi
    ```

2. **Create a Build Directory**:
    ```sh
    mkdir build
    cd build
    ```

3. **Run CMake**:
    ```sh
    cmake ..
    ```

4. **Build the Project**:
    ```sh
    make
    ```

## Running the Compiler

To run the compiler on a source file:

```sh
./lipi path/to/your/source_file.lipi
>>>>>>
