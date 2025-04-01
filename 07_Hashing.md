### **Introduction to Hashing**

- Hashing allows **Search, Insert, and Delete in O(1) time on average**.
- It maps **large values to small keys** using a **hash function**.
- Hashing is used in data structures like **hash tables, sets, and maps**.

---

### **Direct Address Table (Perfect Hashing)**

- Works when the key range is **small and known in advance**.
- Example: If **x is in the range [0, 999]**, we can use a direct address table with an array of size 1000.
- **Operations**:
  - **Insert:** Set `hash[x] = 1` to mark presence.
  - **Delete:** Set `hash[x] = 0` to remove the element.
  - **Search:** Simply return `hash[x]`, which is either 0 (absent) or 1 (present).

⚡ **Drawback:** Requires **O(N) space**, even if only a few keys are used.

---

### **Hash Function**

- Converts a **large input value** into a **smaller key** in the range `[0, m-1]`.
- A common technique is **Modulo-based Hashing**, where `x % m` is used to determine the hash index, with `m` being a prime number.
- **Desirable properties of a good hash function**:
   - **Fast computation** to maintain efficiency.
   - **Uniform distribution** to minimize collisions.
   - **Deterministic** so that the same input always maps to the same output.

---

### **Collision Handling**

Since multiple inputs can map to the **same key**, we need to handle **collisions**:

1. **Chaining (Separate Chaining)**
   - Each hash table index stores a **linked list or vector**.
   - When a collision occurs, we **append** the new element to the list.
   - **Insertion, Search, and Delete take O(1) on average**, assuming a good hash function.

2. **Open Addressing**
   - If a collision occurs, search for an empty slot within the table.
   - Common methods:
     - **Linear Probing:** Check the next available slot, moving sequentially.
     - **Quadratic Probing:** Check slots farther away, using a squared step size (1², 2², 3², ...).
     - **Double Hashing:** Use a second hash function to determine the step size, reducing clustering.

---

### **Questions**

#### **Easy**
- [Two Sum](https://leetcode.com/problems/two-sum/description/)
- [Count Elements With Maximum Frequency](https://leetcode.com/problems/count-elements-with-maximum-frequency/description/)
- [Relative Sort Array](https://leetcode.com/problems/relative-sort-array/description/)
- [Union of Arrays with Duplicates](https://www.geeksforgeeks.org/problems/union-of-two-arrays3538/1)
- [Intersection of Two Arrays](https://leetcode.com/problems/intersection-of-two-arrays/description/)
- [Intersection of Two Arrays II](https://leetcode.com/problems/intersection-of-two-arrays-ii/description/)

#### **Medium**
- [Group Anagrams](https://leetcode.com/problems/group-anagrams/description/)
- [Subarray with Zero Sum](https://www.geeksforgeeks.org/problems/subarray-with-0-sum-1587115621/1)
- [Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/description/)
- [Longest Subarray with Sum K](https://www.geeksforgeeks.org/problems/longest-sub-array-with-sum-k0809/1)
- [Contiguous Array](https://leetcode.com/problems/contiguous-array/description/)
- [Longest Span in Two Binary Arrays](https://www.geeksforgeeks.org/problems/longest-span-with-same-sum-in-two-binary-arrays5142/1)
- [Binary Subarrays With Sum](https://leetcode.com/problems/binary-subarrays-with-sum/description/)
- [Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/description/)
- [Count Distinct Elements in Every Window](https://www.geeksforgeeks.org/problems/count-distinct-elements-in-every-window/1)
- [Check If Array Pairs Are Divisible by K](https://leetcode.com/problems/check-if-array-pairs-are-divisible-by-k/description/)
- [Count Pairs in Array Divisible by K](https://www.geeksforgeeks.org/problems/count-pairs-in-array-divisible-by-k/1)
- [Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
- [Longest Subarray with Sum Divisible by K](https://www.geeksforgeeks.org/problems/longest-subarray-with-sum-divisible-by-k1259/1)

#### **Hard**
- [4 Sum – Count Quadruplets with Given Sum](https://www.geeksforgeeks.org/problems/count-quadruplets-with-given-sum/1)
- [Subarrays with K Different Integers](https://leetcode.com/problems/subarrays-with-k-different-integers/description/)
- [Max Points on a Line](https://leetcode.com/problems/max-points-on-a-line/description/)
