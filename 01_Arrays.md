### Arrays

- **Declaration:**
    - `int arr[5];` — Declares an array of size 5.
    - `int arr[n];` — Declares an array with size `n`.
    - `int arr[] = {1, 2, 3, 4, 5};` — Initializes an array with specific values.
    - `int arr[5] = {0};` — Initializes all elements to 0.
    - `int arr[5] = {1};` — Initializes the first element to 1 and the rest to 0.
    - `int arr[] = {1, 2, 3, 4, 5};` — Initializes with 5 elements.
    - `int n = sizeof(arr) / sizeof(arr[0]);` — Calculates the number of elements in the array.

---

### Traversal

- **Methods:**
    - `for(int i = 0; i < arr.size(); i++)` — Loop through the array using index.
    - `for(int x : arr)` — Range-based for loop (value).
    - `for(int &x : arr)` — Range-based for loop (reference).
    - `for(auto x : arr)` — Auto keyword to infer type.
    - `for(auto &x : arr)` — Auto with reference.

---

### Array vs Pointers

- **Example:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[] = {1, 2, 3, 4, 5, 6};  // Array of 6 elements
    int *ptr = arr;  // Pointer pointing to the first element of the array

    // Size of array vs pointer
    cout << sizeof(arr) << " " << sizeof(ptr) << endl;  // sizeof(arr) is the total size of the array, sizeof(ptr) is the size of the pointer itself

    // Accessing elements using array and pointer (both give the same result)
    cout << *(arr + 2) << " " << arr[2] << " " << *(ptr + 2) << " " << ptr[2] << " " << 2[arr] << " " << 2[ptr] << endl;  // Access elements using array and pointer syntax (interchangeable)

    // What you can't do with arr that you can do with ptr
    ptr = ptr + 2;  // You can reassign a pointer to point to any location in memory.
    cout << *ptr << endl;  // After ptr is moved, it points to the third element (value: 3)

    // What you can't do with arr:
    // arr = arr + 2;  // Error: You cannot change the address of the array itself. `arr` is a constant pointer.
    
    return 0;
}
```

---

### Types of Arrays

- **Fixed-Sized Arrays:**
    - Allocated on the stack: `int arr[n];`
    - Allocated on the heap: `int *arr = new int[n];`

- **Dynamic-Sized Arrays:**
    - `vector<int> v;` — A dynamic array (vector) in C++.

---

### Questions

#### Basic

- Sum of an Array
- Average of an Array
- Median of an Array
- Subarray vs Subsets vs Subsequence

#### Easy

- Miscellaneous:
    - [Reverse an Array](https://www.geeksforgeeks.org/problems/reverse-an-array/0)
    - [Reverse Array in Groups](https://www.geeksforgeeks.org/problems/reverse-array-in-groups0255/1)
    - [Check if Array is Sorted](https://www.geeksforgeeks.org/problems/check-if-an-array-is-sorted0701/1)
    - [Find Pivot Index](https://leetcode.com/problems/find-pivot-index/description/)
    - [Convert Array into Zig-Zag Fashion](https://www.geeksforgeeks.org/problems/convert-array-into-zig-zag-fashion1638/1)

- Max-Min (Single Pass Algorithms):
    - [Largest Element in Array](https://www.geeksforgeeks.org/problems/largest-element-in-array4009/1)
    - [Second Largest](https://www.geeksforgeeks.org/problems/second-largest3735/1)
    - [Third Largest Element](https://www.geeksforgeeks.org/problems/third-largest-element/1)
    - [Leaders in an Array](https://www.geeksforgeeks.org/problems/leaders-in-an-array-1587115620/1)
    - [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/description/)

- Counters:
    - [Max Consecutive Ones](https://leetcode.com/problems/max-consecutive-ones/description/)

- Two Pointers:
    - [Move Zeroes](https://leetcode.com/problems/move-zeroes/description/)
    - [Two Sum](https://www.geeksforgeeks.org/problems/key-pair5616/1)
    - [Triplet Sum in Array](https://www.geeksforgeeks.org/problems/triplet-sum-in-array-1587115621/1)
    - [Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/description/)

- Cycle Sort:
    - [Missing Number](https://leetcode.com/problems/missing-number/description/)
    - [Missing And Repeating](https://www.geeksforgeeks.org/problems/find-missing-and-repeating2512/1)

- Pre Computation:
    - [Prefix Sum - Range Sum Query](https://leetcode.com/problems/range-sum-query-immutable/description/)

#### Medium

- Two Pointers:
    - [Pair Sum in a Sorted and Rotated Array](https://www.geeksforgeeks.org/problems/pair-sum-in-a-sorted-and-rotated-array/1)
    - [Count pair sum in sorted array](https://www.geeksforgeeks.org/problems/pair-with-given-sum-in-a-sorted-array4940/1)
    - [Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/description/)
    - [Container With Most Water](https://leetcode.com/problems/container-with-most-water/description/)

- Three Pointers:
    - [Sort Colors](https://leetcode.com/problems/sort-colors/description/)
    - [Common in 3 Sorted Arrays](https://www.geeksforgeeks.org/problems/common-elements1132/1)
    - [Merge Three Sorted Arrays](https://www.geeksforgeeks.org/problems/merge-three-sorted-arrays-1587115620/0)

- Sliding Window:
    - [Max Sum Subarray of Size K](https://www.geeksforgeeks.org/problems/max-sum-subarray-of-size-k5313/1)
    - [Minimum Swaps to Group All 1's Together II](https://leetcode.com/problems/minimum-swaps-to-group-all-1s-together-ii/description/)
    - [Minimum swaps and K together](https://www.geeksforgeeks.org/problems/minimum-swaps-required-to-bring-all-elements-less-than-or-equal-to-k-together4847/1)
    - [Subarray with Given Sum](https://www.geeksforgeeks.org/problems/subarray-with-given-sum-1587115621/1)
    - [Minimum Size Subarray Sum](https://leetcode.com/problems/minimum-size-subarray-sum/description/)
    - [Binary Subarrays With Sum](https://leetcode.com/problems/binary-subarrays-with-sum/description/) [Use O(1) space]
    - [Maximum Subarray Sum – Kadane’s Algorithm](https://leetcode.com/problems/maximum-subarray/)
    - [Maximum Sum Circular Subarray](https://leetcode.com/problems/maximum-sum-circular-subarray/description/)
    - [Maximize i*arr[i] among all Rotations of Array](https://www.geeksforgeeks.org/problems/max-sum-in-the-configuration/1)

- Miscellaneous:
    - [Rotate Array by K Places](https://leetcode.com/problems/rotate-array/description/)
    - [Best Time to Buy and Sell Stock II](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-ii/description/)
    - [Majority Element](https://leetcode.com/problems/majority-element/) + [Majority Element (-1 case)](https://www.geeksforgeeks.org/problems/majority-element-1587115620/1)
    - [Majority Element II](https://leetcode.com/problems/majority-element-ii/description/)
    - [Sum of All Subarrays](https://www.geeksforgeeks.org/problems/sum-of-subarrays2229/1)
    - [Maximum Product Subarray](https://leetcode.com/problems/maximum-product-subarray/description/)
    - [Next Permutation](https://leetcode.com/problems/next-permutation/description/)
    - [Factorials of Large Numbers](https://www.geeksforgeeks.org/problems/factorials-of-large-numbers2508/1)
    - [Jump Game II](https://leetcode.com/problems/jump-game-ii/description/) + [Minimum Jumps to Reach End (-1 case)](https://www.geeksforgeeks.org/problems/minimum-number-of-jumps-1587115620/1)
    - [Rearrange Array in Max Min Form in O(1) Space](https://www.geeksforgeeks.org/problems/-rearrange-array-alternately-1587115620/1)
    - [Rearrange Array Elements by Sign](https://leetcode.com/problems/rearrange-array-elements-by-sign/description/)

#### Hard

- [First Missing Positive](https://leetcode.com/problems/first-missing-positive/description/)
- [Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/description/)
- [Best Time to Buy and Sell Stock III](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-iii/description/)
- [Find the Closest Palindrome](https://leetcode.com/problems/find-the-closest-palindrome/description/)
