# References

A **reference** in C++ allows modification of the original variable. It provides an alias for another variable.

## Creating References
- **Syntax**: `int &y = x;`  
  `y` is a reference to `x`, meaning any modification to `y` will modify `x`.

### Example of Reference in Functions:
- A function that swaps two values:
  ```cpp
  void swap(int &x, int &y) {
      int temp = x;
      x = y;
      y = temp;
  }
  ```

- **Range-based for loop with reference**:
  ```cpp
  for(int &x : arr) {
      x = 0;  // Modifies the original element in the array
  }
  ```

### Avoiding Copy (Passing by Reference):
- **Passing vectors or large objects by reference** to avoid copying:
  ```cpp
  void fun(vector<int> &v) {}
  ```

- **Auto reference in a loop**:
  ```cpp
  for(auto& arr : mat) {}
  ```

---

# Address Operator

The **address operator** (`&`) retrieves the memory address of a variable.

### Example:
```cpp
int x = 10;
print(&x, *(&x));  // Prints the address of x and the value of x
```

---

# Pointers

A **pointer** holds the memory address of a variable. You can manipulate data by dereferencing a pointer.

## Example:
```cpp
int x = 10;
int *p = &x;
print(x, &x, p, *p);  // 10, address of x, address of x, 10
```

### Pointer Types:
- **Integer pointer**:
  ```cpp
  int *p1;
  ```
- **Double pointer**:
  ```cpp
  double *p2;
  ```
- **String pointer**:
  ```cpp
  string *p3;
  ```
- **Pointer size**:
  ```cpp
  print(sizeof(p1), sizeof(p2), sizeof(p3));  // Typically prints 8 bytes for each pointer on a 64-bit system
  ```

---

# Null vs nullptr

- **Null**: `int x = NULL;` is allowed but not recommended.
- **nullptr**: `int x = nullptr;` is the modern C++ way and avoids issues with null pointers.

---

# Pointer Arithmetic

Pointers can be incremented or decremented to traverse arrays or memory blocks.

### Example:
```cpp
int arr[] = {10, 20, 30, 40};
int *ptr = arr;
print(*ptr, ptr);  // 10, address of arr[0]
ptr++;             // ptr = ptr + 1
print(*ptr, ptr);  // 20, address of arr[1]
ptr--;             // ptr = ptr - 1
print(*ptr, ptr);  // 10, address of arr[0]
int *ptr2 = ptr + 3;
print(ptr2 - ptr); // Prints 3 (distance between pointers)
```

---

# Dynamic Memory Allocation

In C++, memory is allocated on the **stack** or **heap**.

## Stack vs Heap

- **Stack**: Memory is automatically allocated and deallocated.
  ```cpp
  int a = 10;
  int a[10];
  ```

- **Heap**: Memory is dynamically allocated using `new` and must be explicitly deallocated with `delete`.
  ```cpp
  int *ptr = new int(5);  // Dynamically allocated memory for an integer
  delete ptr;             // Freeing the memory

  int *ptr = new int[5];  // Dynamically allocated array
  int *ptr = new int[5]{};  // Dynamically allocated and initialized array
  delete[] ptr;             // Freeing dynamically allocated array
  ```

### Important:
- **Never access memory after it is deleted** to avoid undefined behavior.

---

### Array Decay and Size Calculation Issue:

This code illustrates **array decay** (how an array decays into a pointer when passed to a function) and demonstrates why calculating the size of an array using `sizeof(arr)` inside a function is incorrect.

```cpp
#include <iostream>
using namespace std;

void fun(int arr[]) {
    // This is wrong: The array decays to a pointer, so sizeof(arr) will give the size of the pointer, not the array size
    int n = sizeof(arr) / sizeof(arr[0]);
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
}

int main() {
    int arr[] = {10, 20, 30, 40, 50};
    // This works correctly: We calculate the array size in the main function
    int n = sizeof(arr) / sizeof(arr[0]);

    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;

    fun(arr);  // Call to the function (array decay occurs here)

    return 0;
}
```

### Output:
```
10 20 30 40 50
10 20 30 40 50
```

### Explanation:
- **Array Decay**: When the array `arr` is passed to the function `fun()`, it decays into a pointer, losing its size information. The `sizeof(arr)` in the function will now return the size of the pointer, not the size of the original array.
  
  To correctly calculate the number of elements in the array when passing it to a function, we should either pass the array size as an additional argument or use `std::vector` (which retains its size information).
  
