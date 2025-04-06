### **C Style String**

- `char s1[] = "hello";`
  - This initializes a **C-style string** using a character array. It automatically appends a **null terminator (`\0`)** at the end to mark the end of the string.
  
- `char s1[] = {'h','e','l','l','o'}; // Necessary \0`
  - This is an alternative way to initialize a C-style string, manually specifying each character. However, the null terminator (`\0`) is necessary at the end of the string to denote the string’s end.

---

### **C++ String**

- `string str = "hello";`
  - This initializes a **C++ string** using the `string` class, which is more flexible than C-style strings. It handles memory management and includes many built-in functions for string manipulation.

- **Comparison Operators**: `<`, `>`, `<=`, `>=`, etc.
  - These operators can be used to compare strings lexicographically (i.e., based on their alphabetical order).

- `str.substr()`
  - This function is used to extract a **substring** from a string, starting from a specified index.

- `str.find()`
  - This function finds the first occurrence of a substring or character in the string and returns its index.

---

### **Questions**

#### **Basic**
- [Binary To Decimal](https://www.geeksforgeeks.org/problems/binary-number-to-decimal-number3525/1)
- [Decimal To Binary](https://www.geeksforgeeks.org/problems/decimal-to-binary-1587115620/1)

#### **Easy**
- [Check if Strings are Rotations](https://leetcode.com/problems/rotate-string/description/)
- [Valid Anagram](https://leetcode.com/problems/valid-anagram/description/)
- [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/description/)
- [Valid Palindrome II](https://leetcode.com/problems/valid-palindrome-ii/description/)
- [Isomorphic Strings](https://leetcode.com/problems/isomorphic-strings/description/)
- [Is Subsequence](https://leetcode.com/problems/is-subsequence/description/)
- [First Repeated Character](https://www.geeksforgeeks.org/problems/find-first-repeated-character4108/1)
- [First Unique Character in a String](https://leetcode.com/problems/first-unique-character-in-a-string/description/)
- [Largest Odd Number in String](https://leetcode.com/problems/largest-odd-number-in-string/description/)
- [Roman to Integer](https://leetcode.com/problems/roman-to-integer/description/)
- [Add Strings](https://leetcode.com/problems/add-strings/description/)
- [Pattern Searching - Naive](https://www.geeksforgeeks.org/problems/pattern-searching5231/1)

#### **Medium**
- [Minimum Add to Make Parentheses Valid](https://leetcode.com/problems/minimum-add-to-make-parentheses-valid/description/)
- [Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string/description/)
- [String to Integer (atoi)](https://leetcode.com/problems/string-to-integer-atoi/description/)
- [Count and Say](https://leetcode.com/problems/count-and-say/description/)
- [Sort Characters By Frequency](https://leetcode.com/problems/sort-characters-by-frequency/description/)
- [Find All Anagrams in a String](https://leetcode.com/problems/find-all-anagrams-in-a-string/description/)
- [Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/description/)
- [Pattern Searching - Rabin Karp Algorithm](https://www.geeksforgeeks.org/problems/search-pattern-rabin-karp-algorithm--141631/1)
- [Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/description/)
- [Compare Version Numbers](https://leetcode.com/problems/compare-version-numbers/description/)

#### **Hard**
- [Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/description/)
- [Substrings with K Distinct](https://www.geeksforgeeks.org/problems/count-number-of-substrings4528/1)
- [Pattern Searching - KMP](https://www.geeksforgeeks.org/problems/search-pattern0205/1)
- [Shortest Palindrome](https://leetcode.com/problems/shortest-palindrome/description/)
- [Integer to English Words](https://leetcode.com/problems/integer-to-english-words/description/)
