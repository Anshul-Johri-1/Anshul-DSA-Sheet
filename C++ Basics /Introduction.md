# Programming Basics / Introduction

## 1. Compiler VS Interpreter
- **Compiler**: Translates the entire program into machine code before execution.
- **Interpreter**: Translates and executes the program line by line.

## 2. Statically Typed vs Dynamically Typed
- **Statically Typed**: Variables must be declared with a type at compile time.
- **Dynamically Typed**: Variable types are determined at runtime.

## 3. Keywords vs Identifiers
- **Keywords**: Reserved words in the programming language (e.g., `int`, `float`, `return`).
- **Identifiers**: Names given to variables, functions, etc.

## 4. Header Files
Header files contain definitions of functions, macros, and constants.

## 5. Namespace
Namespaces allow the organization of code into logical groups to prevent name collisions.

## 6. First C++ Program
```
# include <iostream>
using namespace std;

int main() {
    cout << "Hello World";
    return 0;
}
```

## 7. Comments
- **Single-line comment**: // This is a comment
- **Multi-line comment**: /* This is a multi-line comment */

## 8. Identifier Naming Rules
- Identifiers must begin with a letter or an underscore.
- Subsequent characters can include letters, digits, and underscores.

## 9. Data Types

### Primitive Data Types
- **short, int, long, long long, char**
- **unsigned**
- **float, double, long double**
- **bool, void**

### Non-Primitive Data Types
- Arrays, vectors, strings, pointers, user-defined types.

## 10. sizeof Operator
The sizeof operator returns the size of a data type or variable in bytes.
| Data Type             | No. of Bits | Range                                   | Mathematical Representation           |
|-----------------------|-------------|-----------------------------------------|----------------------------------------|
| char                  | 8           | -128 to 127                             | (-2⁷ to 2⁷ - 1)                       |
| unsigned char         | 8           | 0 to 255                                | (0 to 2⁸ - 1)                         |
| short                 | 16          | -32,768 to 32,767                       | (-2¹⁵ to 2¹⁵ - 1)                     |
| int                   | 32          | ≈ -2.14 × 10⁹ to 2.14 × 10⁹            | (-2³¹ to 2³¹ - 1)                     |
| unsigned int          | 32          | 0 to ≈ 4.29 × 10⁹                       | (0 to 2³² - 1)                        |
| long long             | 64          | ≈ -9.2 × 10¹⁸ to 9.2 × 10¹⁸            | (-2⁶³ to 2⁶³ - 1)                     |
| unsigned long long    | 64          | 0 to ≈ 1.8 × 10¹⁹                      | (0 to 2⁶⁴ - 1)                        |
| float                 | 32          | ±1.18 × 10⁻³⁸ to ±3.4 × 10³⁸           | (±2⁻¹²⁶ to ±2¹²⁸)                    |
| double                | 64          | ±2.23 × 10⁻³⁰⁸ to ±1.80 × 10³⁰⁸       | (±2⁻¹⁰²² to ±2¹⁰²⁴)                  |
| bool                  | 8           | 0 to 1                                  | (0 to 1)                              |


## 11. Scope of Variables
- Variables have different scopes (function, loop, or block scope).
- static keyword restricts the lifetime of a variable to the duration of the program.

## 12. Keywords: static, const, auto, etc.
- const: Makes a variable immutable.
- auto: Automatically deduces the type of a variable.
- static: Ensures the variable retains its value between function calls and limits its scope to the function or file.

## 13. Data Types and Literals

### Integer Literals
- Decimal: int x = 9;
- Hexadecimal: int x = 0xF;
- Octal: int x = 07;
- Binary: int x = 0b01;
- Long Long: long long int x = 2ll;

### Floating Point Literals
- float x = 10.515f;
- double x = 10.515;
- long double x = 10.515l;

### Scientific Notation
- float x = 2.1e15f;
- double x = 2.1e15;
- long double x = 2.1e15l;

### Character and String
- char
- string

## 14. Type Conversion

### Implicit Conversion
- Implicit conversion happens automatically by the compiler.
    ```int x = 10.5;```

### Explicit Conversion
- Explicit conversion requires the use of a cast.
    ```double z = double(x) / y;```

### Conversion Order
- bool → char → int → long long → float → double → long double

## 15. Input and Output

### Input
```
cin >> x >> y;
getline(cin, name);
```
### Output
```
cout << x << " " << y << endl;
```

- **Other Output Streams**: cerr, ifstream, ofstream
- **Setting precision**: cout << fixed << setprecision(5);

## 16. Simple Program Example
```
int x, y;
cout << "Enter x: ";
cin >> x;
cout << "Enter y: ";
cin >> y;
cout << "Multiplication of " << x << " and " << y << " is: " << x * y << endl;
```

## 17. Escape Sequences
- `\n` : Newline
- `\'` : Single quote
- `\"` : Double quote
- `\t` : Tab
- `\0` : Null character
- `\\` : Backslash

## 18. Operators
- **Unary Operators:** `++`, `--`
- **Arithmetic Operators:** `+`, `-`, `*`, `/`, `%`
- **Relational Operators:** `<`, `<=`, `>`, `>=`, `==`, `!=`
- **Logical Operators:** `&&`, `||`, `!`
- **Bitwise Operators:** `&`, `|`, `<<`, `>>`, `~`, `^`
- **Assignment Operators:** `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `&=`, `|=`, `<<=`, `>>=`, `^=`
- **Ternary or Conditional Operator:** `?:`

# Operator Precedence
1. **Unary Operators:** `!`, `++`, `--`
2. **Arithmetic Operators:** `*`, `/`, `%`
3. **Unary Operators:** `+`, `-`
4. **Relational Operators:** `<`, `<=`, `>=`, `>`
5. **Equality Operators:** `==`, `!=`
6. **Logical AND:** `&&`
7. **Logical OR:** `||`
8. **Assignment Operator:** `=`


## 19. Questions for Practice
1. [Leap Year](https://www.geeksforgeeks.org/problems/leap-year0943/1) using Ternary
2. Last Digit of a Number
3. First Digit of a Number
4. Sum of Digits of a Number
5. Reverse a Number
