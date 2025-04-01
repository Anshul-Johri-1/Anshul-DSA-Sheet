### **Function Executions**

- **Statements are executed line-by-line**:
  - Functions execute sequentially, starting from the top and moving down, with control transferred to other functions when they are called.

- **Example Code**:
  ```cpp
  void fun1() {  
      cout << "fun1\n";  
  }

  void fun2() {  
      cout << "Before fun1\n";  
      fun1();  
      cout << "After fun1\n";  
  }

  int main() {  
      cout << "Before fun2\n";  
      fun2();  
      cout << "After fun2\n";  
      return 0;  
  }
  ```

---

### **Output**:
- Before fun2  
- Before fun1  
- fun1  
- After fun1  
- After fun2

---

### **Recursion Dry Run**

- **Recursive Function Example**:
  ```cpp
  void fun(int n) {  
      if (n == 0) {  
          return;  
      }  
      cout << n << endl;  
      fun(n - 1);  
      cout << n << endl;  
  }
  ```

- **Another Recursive Function Example**:
  ```cpp
  int fun(int n) {  
      if (n == 1)  
          return 0;  
      return 1 + fun(n / 2);  
  }
  ```

---

### **Recursion Concept**

#### **Easy**
- `void Print_N_to_1() {}`  
- `void Print_1_to_N() {}`
- `int sumOfDigit(int num) {}`  
- `int factorial(int n) {}`  
- `int Fib(int n) {}`  
- `bool isPalindrome(string &str, int lo, int hi) {}`
- `void towerOfHanoi() {}`  
- [Josephus Problem](https://leetcode.com/problems/find-the-winner-of-the-circular-game/description/)

---

### **Questions (Backtracking)**

#### **Medium**
- [Word Search](https://leetcode.com/problems/word-search/description/)  
- [Rat in a Maze Problem](https://www.geeksforgeeks.org/problems/rat-in-a-maze-problem/1)  
- [Generate Parentheses](https://leetcode.com/problems/generate-parentheses/description/)  
- [Subsets](https://leetcode.com/problems/subsets/description/)  
- [Subsets II](https://leetcode.com/problems/subsets-ii/description/)  
- [Permutations](https://leetcode.com/problems/permutations/description/)  
- [Permutations II](https://leetcode.com/problems/permutations-ii/description/)  
- [Combination Sum](https://leetcode.com/problems/combination-sum/description/)  
- [Combination Sum II](https://leetcode.com/problems/combination-sum-ii/description/)  
- [Combination Sum III](https://leetcode.com/problems/combination-sum-iii/description/)  
- [Palindrome Partitioning](https://leetcode.com/problems/palindrome-partitioning/description/)  
- [Restore IP Addresses](https://leetcode.com/problems/restore-ip-addresses/description/)

#### **Hard**
- [N-Queens](https://leetcode.com/problems/n-queens/description/)  
- [N-Queens II](https://leetcode.com/problems/n-queens-ii/description/)  
- [Sudoku Solver](https://leetcode.com/problems/sudoku-solver/description/)  
- [Word Break II](https://leetcode.com/problems/word-break-ii/)
