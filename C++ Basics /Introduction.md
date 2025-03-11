### Compiler vs Interpreter
- **Compiler** translates the entire program into machine code at once.
- **Interpreter** translates and executes code line by line.

### Statically Typed vs Dynamically Typed
- **Statically Typed**: Variable types are defined at compile time (e.g., C++).
- **Dynamically Typed**: Variable types are determined at runtime (e.g., Python).

### Keywords vs Identifiers
- **Keywords**: Reserved words in C++ (e.g., `int`, `return`, `class`).
- **Identifiers**: Names given to variables, functions, etc. (e.g., `x`, `myFunction`).

### Header Files
- Include files that declare functions, classes, and variables (e.g., `<iostream>`).

### Namespace
- A scope to organize code and avoid name conflicts. C++ uses `namespace std`.

### First C++ Program Example
```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello World";
    return 0;
}
```

### Comments
- **Single-line**: `// comment`
- **Multi-line**: `/* comment */`

### Identifier Naming Rules
- Must start with a letter or underscore.
- Can contain letters, digits, and underscores.
- Cannot be a keyword.

### Data Types

#### Primitive Types
- **Integer**: `short`, `int`, `long`, `long long`, `char`
- **Unsigned**: `unsigned short`, `unsigned int`, etc.
- **Floating Point**: `float`, `double`, `long double`
- **Boolean**: `bool`
- **Void**: No type

#### Non-Primitive Types
- **Arrays**, **Vectors**, **Strings**, **Pointers**, **User-defined types**

### Sizeof Operator
- Returns the size (in bytes) of a data type or object.

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

### Variable Scope
- **Block Scope**: Variables inside curly brackets `{}`.
- **Global Scope**: Variables defined outside functions.

### Static Keyword
- Retains variable value between function calls.

### Const Keyword
- Used to define constants.

### Auto Keyword
- Automatically infers the type of the variable.

### Literals

Literals are fixed values used in programming that represent data directly.

#### Integer Literals
- **Decimal**: `int x = 9;`
- **Hexadecimal**: `int x = 0xF;` (Starts with `0x` for hex numbers)
- **Octal**: `int x = 07;` (Starts with `0` for octal numbers)
- **Binary**: `int x = 0b01;` (Starts with `0b` for binary numbers)
- **Long Long Integer**: `long long int x = 2ll;` (Ends with `ll` for long long)

#### Floating-point Literals
- **float**: `float x = 10.515f;` (Ends with `f` for float)
- **double**: `double x = 10.515;` (Default type for floating-point literals)
- **long double**: `long double x = 10.515l;` (Ends with `l` for long double)

#### Exponential Notation
- **float**: `float x = 2.1e15f;` (Scientific notation for floating-point)
- **double**: `double x = 2.1e15;`
- **long double**: `long double x = 2.1e15l;`

#### Character Literals
- **char**: `'A'` (Single characters enclosed in single quotes)
- **Escape Sequences**: `'\\'`, `'\n'`, `'\t'`

#### String Literals
- **string**: `"Hello, World!"` (Strings are enclosed in double quotes)

### Type Conversion

#### Implicit Conversion
- Automatically done by the compiler (e.g., `int x = 10.5;`).

#### Explicit Conversion
- Done using casting (e.g., `double x = double(15) / 2;`).

#### Conversion Order
- `bool → char → int → long long → float → double → long double`

### Input/Output

- **Input**: `cin >> x;`, `getline(cin, name);`
- **Output**: `cout << x << " " << y << endl;`, `cerr` for errors.
- **File I/O**: `ifstream`, `ofstream`

#### Format Output
- `cout << fixed << setprecision(5);`

### Simple Program Example
```cpp
int x, y;
cout << "Enter x: ";
cin >> x;
cout << "Enter y: ";
cin >> y;
cout << "Multiplication of " << x << " and " << y << " is: " << x * y << endl;
```

### Escape Sequences
- `\n` (new line)
- `\'` (single quote)
- `\"` (double quote)
- `\t` (tab)
- `\0` (null character)
- `\\` (backslash)

### Operators
- **Unary Operators:** `++`, `--`
- **Arithmetic Operators:** `+`, `-`, `*`, `/`, `%`
- **Relational Operators:** `<`, `<=`, `>`, `>=`, `==`, `!=`
- **Logical Operators:** `&&`, `||`, `!`
- **Bitwise Operators:** `&`, `|`, `<<`, `>>`, `~`, `^`
- **Assignment Operators:** `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `&=`, `|=`, `<<=`, `>>=`, `^=`
- **Ternary or Conditional Operator:** `?:`

#### Operator Precedence
1. **Unary Operators:** `!`, `++`, `--`
2. **Arithmetic Operators:** `*`, `/`, `%`
3. **Unary Operators:** `+`, `-`
4. **Relational Operators:** `<`, `<=`, `>=`, `>`
5. **Equality Operators:** `==`, `!=`
6. **Logical AND:** `&&`
7. **Logical OR:** `||`
8. **Assignment Operator:** `=`

### Questions for Practice
1. [Leap Year](https://www.geeksforgeeks.org/problems/leap-year0943/1) using Ternary
2. Last Digit of a Number
3. First Digit of a Number
4. Sum of Digits of a Number
5. Reverse a Number
