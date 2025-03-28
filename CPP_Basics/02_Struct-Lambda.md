## Struct

A `struct` is a user-defined data type that groups related variables together. In C++, `struct` members are public by default, and they can store multiple data types.

### Example of Struct
```cpp
struct Point {
    int x;
    int y;
};
```

### Creating and Using a Struct
- **Dynamic Allocation** (using `new`):
  ```cpp
  Point *p = new Point();
  p->x = 10;
  p->y = 5;
  ```

- **Static Allocation**:
  ```cpp
  Point p;
  p.x = 10;
  p.y = 5;
  ```

### Struct with Multiple Data Types
```cpp
struct Student {
    int rollNo;
    string name;
    string address;
};
Student me = {10, "Anshul", "Delhi"};
```

### Struct vs Class
- **Struct**: Members are **public** by default.
- **Class**: Members are **private** by default unless specified.

## Lambda Functions

A lambda function is an anonymous function that can be used to create short function objects.

### Basic Syntax of Lambda
```cpp
auto lambda = [](int a, int b) -> bool {
    return a < b;
};
```

### Example Usage in Sorting
```cpp
bool cmp(int a, int b) {
    return a < b;
}

sort(arr.begin(), arr.end(), cmp);  // Traditional function
```

Using a **lambda function** in `sort()`:
```cpp
sort(arr.begin(), arr.end(), [](int a, int b) -> bool {
    return a < b;
});
```

### Capture List
The **capture list** defines how external variables are passed into the lambda. It can capture variables by **value** or by **reference**.

#### Capture List Syntax:
- `[]`: Captures nothing.
- `[=]`: Captures variables by **value**.
- `[&]`: Captures variables by **reference**.
- `[=, &x]`: Captures all by **value** except `x`, which is captured by **reference**.
- `[&, x]`: Captures all by **reference** except `x`, which is captured by **value**.
