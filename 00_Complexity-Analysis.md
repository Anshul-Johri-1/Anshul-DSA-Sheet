### **Time Complexity Notations**

- **Big O (O)**: Represents the **upper bound** of the running time. It gives the **worst-case** scenario for an algorithm. It’s used to describe the maximum time an algorithm can take.
  
- **Theta (Θ)**: Represents the **exact** time complexity of an algorithm. It gives both the **upper and lower bound**, meaning it describes the **average-case** time.

- **Omega (Ω)**: Represents the **lower bound** of the running time. It gives the **best-case** scenario, describing the minimum time an algorithm will take.

### **Examples with Common Time Complexities**

1. **O(1) - Constant Time**
   - The time taken doesn't depend on the input size. The algorithm always runs in the same time.
   - **Example**:

     ```cpp
     cout << "HI";  // Just prints "HI", takes constant time
     ```

2. **O(log n) - Logarithmic Time**
   - The time grows logarithmically as the input size increases. Often seen in algorithms that divide the input in half, like binary search.
   - **Example**:

     ```cpp
     for (int i = 1; i < n; i *= 2) {  // Doubling i each time
         cout << i << " ";
     }
     ```
   - The loop runs logarithmically because `i` is doubled each time.

3. **O(n) - Linear Time**
   - The time grows directly in proportion to the input size.
   - **Example**:

     ```cpp
     for (int i = 0; i < n; i++) {  // Looping through each element
         cout << i << " ";
     }
     ```
   - The loop runs once for each element, so it's linear.

4. **O(n log n) - Linearithmic Time**
   - A mix of linear and logarithmic time. Common in divide-and-conquer algorithms like Merge Sort or Quick Sort.
   - **Example**:

     ```cpp
     for (int i = 0; i < n; i++) {        // Linear loop
         for (int j = 0; j < n; j *= 2) { // Logarithmic loop
             cout << i << " " << j << endl;
         }
     }
     ```
   - The outer loop runs `n` times, and the inner loop runs logarithmically, making the overall complexity O(n log n).

5. **O(n^2) - Quadratic Time**
   - The time grows proportionally to the square of the input size. Often seen in algorithms with nested loops.
   - **Example**:

     ```cpp
     for (int i = 0; i < n; i++) {        // Outer loop runs n times
         for (int j = 0; j < n; j++) {    // Inner loop also runs n times
             cout << i << " " << j << endl;
         }
     }
     ```
   - Both loops run `n` times, so the time complexity is O(n^2).

6. **O(2^n) - Exponential Time**
   - The time doubles with each additional element. Common in recursive algorithms that solve problems by trying all possibilities, like the brute force solution to the Traveling Salesman Problem.
   - **Example**:

     ```cpp
     for (int i = 0; i < n; i++) {
         for (int j = 0; j < pow(2, i); j++) {  // Exponential growth
             cout << i << " " << j << endl;
         }
     }
     ```
   - The inner loop runs exponentially with respect to the outer loop's `i`, leading to an O(2^n) time complexity.
