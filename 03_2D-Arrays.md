- **2D Array Initialization**:
  - `int arr[3][2] = {{10, 20}, {30, 40}, {50, 60}};`
  
    A 2D array where each row contains 2 elements, initialized with values.

- **Contiguous Storage**:
  - Elements in 2D arrays are stored in contiguous memory locations, meaning they are sequentially placed in memory.

- **2D Array Initialization (Alternative)**:
  - `int arr[3][2] = {10, 20, 30, 40, 50, 60};`
    
    The same array initialized in a single line without explicitly defining rows.

- **Another 2D Array Initialization**:
  - `int arr[][2] = {{1, 2}, {3, 4}};`
    
    A 2D array with automatic row size determination, where 2 columns are defined.

- **3D Array Initialization**:
  - `int arr[][2][2] = {{{1, 2}, {3, 4}}, {{5, 6}, {7, 8}}};`
    
    A 3D array with 2 blocks, each containing a 2x2 matrix.

---

### **Traversal**

- **Using For Loop**:
  - ```cpp
    for(int i = 0; i < 3; i++) {  
        for(int j = 0; j < 2; j++) {  
            cout << mat[i][j] << " ";
        }
        cout << endl;
    }
    ```

- **Using Range-based For Loop (with Vectors)**:
  - ```cpp
    for(vector<int>& v : mat) {  
        for(int x : v) {  
            cout << x << " "; 
        }
        cout << endl;
    }
    ```

---

### Questions

#### Easy
- [Print Matrix in Snake Pattern](https://www.geeksforgeeks.org/problems/print-matrix-in-snake-pattern-1587115621/1)
- [Matrix Boundary Traversal](https://www.geeksforgeeks.org/problems/boundary-traversal-of-matrix-1587115620/0)

#### Medium
- [Search a 2D Matrix II](https://leetcode.com/problems/search-a-2d-matrix-ii/description/)
- [Set Matrix Zeroes](https://leetcode.com/problems/set-matrix-zeroes/description/)
- [Transpose Matrix](https://leetcode.com/problems/transpose-matrix/description/)
- [Rotate Image](https://leetcode.com/problems/rotate-image/description/)
- [Spiral Matrix](https://leetcode.com/problems/spiral-matrix/description/)
- [Spiral Matrix II](https://leetcode.com/problems/spiral-matrix-ii/description/)
- [Multiply Matrices](https://www.geeksforgeeks.org/problems/multiply-matrices/1)
- [Valid Sudoku](https://leetcode.com/problems/valid-sudoku/description/)

#### Hard
- [Range Sum Query 2D - Immutable](https://leetcode.com/problems/range-sum-query-2d-immutable/description/)
