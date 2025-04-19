### Basic Priority Queue Operations in C++

- `push(x)` – Inserts element `x` into the priority queue  
- `pop()` – Removes the top (highest-priority) element  
- `top()` – Returns the top element without removing it  
- `size()` – Returns the number of elements in the queue  
- `empty()` – Checks whether the queue is empty  

---

### How to Define a Custom Comparator in C++

By default, `priority_queue` in C++ implements a **max heap**. To change the order (e.g., to create a **min heap** or customize behavior), you can define a **comparator** in different ways.

#### 1. Using `greater<int>` for a Min Heap
```cpp
int main() {
    priority_queue<int, vector<int>, greater<>> pq;
}
```

#### 2. Using a Custom Comparator Struct
```cpp
struct cmp {
    bool operator()(int a, int b) {
        return a > b; // min heap behavior
    }
};

int main() {
    priority_queue<int, vector<int>, cmp> pq;
}
```

#### 3. Using a Lambda Comparator
```cpp
int main() {
    auto cmp = [](const auto &a, const auto &b) -> bool {
        return a > b;
    };
    priority_queue<int, vector<int>, decltype(cmp)> pq;
}
```

#### 4. Lambda with External Criteria (e.g., Frequency Map)
```cpp
int main() {
    unordered_map<int, int> freq;
    
    auto cmp = [&freq](const auto &a, const auto &b) -> bool {
        return freq[a] > freq[b]; // lower frequency gets higher priority
    };

    priority_queue<int, vector<int>, decltype(cmp)> pq(cmp);
}
```

---

### Questions

#### Easy
- [Minimum Cost of ropes](https://www.geeksforgeeks.org/problems/minimum-cost-of-ropes-1587115620/1)
- [Kth Largest Element in a Stream](https://leetcode.com/problems/kth-largest-element-in-a-stream/description/)

#### Medium
- [Heap Sort](https://www.geeksforgeeks.org/problems/heap-sort/1)
- [Binary Heap Operations](https://www.geeksforgeeks.org/problems/operations-on-binary-min-heap/1)
- [Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/description/)
- [Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/description/)
- [Merge K Sorted Arrays](https://www.geeksforgeeks.org/problems/merge-k-sorted-arrays/1)
- [Sort K sorted array](https://www.geeksforgeeks.org/problems/nearly-sorted-1587115620/1)
- [K Closest Points to Origin](https://leetcode.com/problems/k-closest-points-to-origin/description/)

#### Hard
- [Meeting Rooms III](https://leetcode.com/problems/meeting-rooms-iii/)
- [Merge K Sorted Linked Lists](https://leetcode.com/problems/merge-k-sorted-lists/description/)
- [Find Median from Data Stream](https://leetcode.com/problems/find-median-from-data-stream/description/)