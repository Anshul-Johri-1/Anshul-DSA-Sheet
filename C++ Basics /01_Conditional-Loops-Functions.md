### If Statement
- **Basic Structure:**
  ```cpp
  if (condition) {
      // Code block if condition is true
  }
  ```
- **Else if (Optional):**
  ```cpp
  if (condition) {
      // Code block if condition is true
  } else if (another_condition) {
      // Code block for second condition
  }
  ```
- **Else (Optional):**
  ```cpp
  if (condition) {
      // Code block if condition is true
  } else {
      // Code block if all conditions are false
  }
  ```

- **Nested If:**
  ```cpp
  if (condition) {
      if (another_condition) {
          // Inner condition logic
      }
  }
  ```

### Switch Statement
- **Basic Structure:**
  ```cpp
  int x = 0, y = 0;
  char move = 'L';
  switch (move) {
      case 'L': x--; break;
      case 'R': x++; break;
      case 'D': y--; break;
      case 'U': y++; break;
      default: cerr << "Wrong Input"; break;
  }
  ```

### Loops
1. **For Loop:**
   ```cpp
   for (int i = 0; i < 10; i++) {
       // Code block
   }
   ```

2. **Range-Based For Loop (C++11 and beyond):**
   ```cpp
   for (auto element : container) {
       // Code block
   }
   ```

3. **While Loop:**
   ```cpp
   while (condition) {
       // Code block
   }
   ```

4. **Do-While Loop:**
   ```cpp
   do {
       // Code block
   } while (condition);
   ```

5. **Nested Loops:**
   ```cpp
   for (int i = 0; i < 5; i++) {
       for (int j = 0; j < 5; j++) {
           // Inner loop code
       }
   }
   ```

6. **Break Statement:**
   ```cpp
   break; // Exits from the loop
   ```

7. **Continue Statement:**
   ```cpp
   continue; // Skips the current iteration and moves to the next
   ```

8. **Star Printing (Exponential Triangle):**
   ```cpp
   for (int i = 0; i < n; i++) {
       for (int j = 0; j < pow(2, n); j++) {
           cout << "*";
       }
       cout << endl;
   }
   ```

### Functions
1. **Function Declaration:**
   ```cpp
   return_type function_name(parameter_list);
   ```

2. **Function Definition:**
   ```cpp
   return_type function_name(parameter_list) {
       // Code block
   }
   ```

3. **Arguments and Parameters:**
   - **Parameter:** Defined in function declaration/definition.
   - **Argument:** Passed during function call.
   
4. **Function Call:**
   ```cpp
   function_name(arguments);
   ```

5. **Function Overloading:**
   Same function name but different parameters.
   ```cpp
   int getMax(int a, int b);
   float getMax(float a, float b);
   ```

6. **Default Arguments:**
   Can be defined either in the declaration or definition.
   ```cpp
   int getSum(int a, int b = 0);
   ```

7. **Function Call Stack:**
   - Functions are called and executed in a stack-like order, returning the result once done.

### Questions on Functions:
- **isPrime Function**

- **Print All Factors**

- **Prime Factorization**

- **Distinct Prime Factors**

- **GCD using Loops**

- **LCM using Loops**

- **Fibonacci Series**
