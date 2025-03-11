### **Binary Representation & Negative Numbers**

#### **1. Binary Representation**

- Uses **0s and 1s** to store data.  
- Example (8-bit): `5 → 00000101`, `13 → 00001101`.

#### **2. Negative Number Representations**

1. **Sign-Magnitude**:
   - MSB (`0` = Positive, `1` = Negative).
   - Example: `-5 → 10000101`.
   - **Issue:** Two representations of `0`.

2. **One’s Complement**:
   - Flip all bits.
   - Example: `-5 → 11111010`.
   - **Issue:** Still two representations of `0`.

3. **Two’s Complement (Standard Method)**:
   - Flip bits & add `1`.
   - Example:
     - `+5 → 00000101`
     - `-5 → 11111011` (flip + add 1).
   - **Advantage:** Single `0`, easy arithmetic.
   - **Range (8-bit):** `-128` to `127`.

#### **3. Quick Checks**

- **MSB = 1?** → Negative in Two’s Complement.
- Convert back: **Flip bits & add 1**, then add `-`.

---

### **Concepts**

- **Bitwise Operators**:
  - `&` (AND)
  - `|` (OR)
  - `^` (XOR)
  - `~` (NOT)
  - `a << b`, equivalent to `a * 2^b` (Left Shift)
  - `a >> b`, equivalent to `a / 2^b` (Right Shift)
  - Set a bit
  - Clear a bit
  - Toggle a bit
  - Check if bit is set
  - Check if a number is odd
  - Strip rightmost set bit

---

### **Questions**

#### **Easy**
- [Swap Two Numbers using Bit Manipulation](https://www.geeksforgeeks.org/problems/swap-two-numbers3844/1)
- [Position of Rightmost Set Bit](https://www.geeksforgeeks.org/problems/find-first-set-bit-1587115620/1)
- [Position of Rightmost Different Bit](https://www.geeksforgeeks.org/problems/rightmost-different-bit-1587115621/1)
- [Count Set Bits](https://leetcode.com/problems/number-of-1-bits/description/)
- [Power of Two](https://leetcode.com/problems/power-of-two/description/)
- [Single Number](https://leetcode.com/problems/single-number/description/)
- [Minimum Bit Flips to Convert Number](https://leetcode.com/problems/minimum-bit-flips-to-convert-number/description/)
- [Toggle Bits from L to R](https://www.geeksforgeeks.org/problems/toggle-bits-given-range0952/1)
- [Add Binary](https://leetcode.com/problems/add-binary/description/)

#### **Medium**
- [Single Number II](https://leetcode.com/problems/single-number-ii/description/)
- [Single Number III](https://leetcode.com/problems/single-number-iii/description/)
- [Power Set using Bitwise](https://leetcode.com/problems/subsets/description/)
- [Divide Two Integers](https://leetcode.com/problems/divide-two-integers/description/)
- [Counting Bits](https://leetcode.com/problems/counting-bits/description/)
- [Count Set Bits from 1 to N](https://www.geeksforgeeks.org/problems/count-total-set-bits-1587115620/1)

#### **Hard**
- (No questions listed)
