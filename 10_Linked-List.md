### Linked Lists

#### Advantages of Linked Lists over Arrays

- **Dynamic Size:** Unlike arrays, linked lists do not require a predefined size and can grow or shrink dynamically without memory reallocation.
- **Efficient Insertions & Deletions:** Inserting or deleting an element in a linked list (given a pointer to the node) is **O(1)**, while in an array, it can take **O(n)** due to shifting elements.
- **No Wasted Memory:** Arrays may have unused allocated space or require resizing, but linked lists use only the memory needed for their elements.
- **No Contiguous Memory Requirement:** Arrays require a continuous memory block, which can be difficult to find for large arrays. Linked lists can utilize scattered memory locations efficiently.
- **Ease of Implementing Data Structures:** Data structures like stacks, queues, and hash tables (with chaining) can be more easily implemented using linked lists than arrays.

---

### Types of Linked Lists

#### Singly Linked List

```cpp
struct Node {  
    int data;  
    Node *next;  
    Node(int x) {  
        data = x;  
        next = nullptr;  
    }  
};

signed main() {  
    Node *a = new Node(10);  
    Node *b = new Node(20);  
    Node *c = new Node(30);

    a->next = b;  
    b->next = c;

    // Alternate way  
    Node *head = new Node(10);  
    head->next = new Node(20);  
    head->next->next = new Node(30);  
}
```

#### Circular Linked List

```cpp
struct Node {  
    int data;  
    Node *next;  
    Node(int x) {  
        data = x;  
        next = nullptr;  
    }  
};

signed main() {  
    Node *a = new Node(10);  
    Node *b = new Node(20);  
    Node *c = new Node(30);

    a->next = b;  
    b->next = c;  
    c->next = a;

    // Alternate way  
    Node *head = new Node(10);  
    head->next = new Node(20);  
    head->next->next = new Node(30);  
    head->next->next->next = head;  
}
```

#### Doubly Linked List

```cpp
struct Node {  
    int data;  
    Node *next, *prev;  
    Node(int x) {  
        data = x;  
        next = nullptr;  
        prev = nullptr;  
    }  
};

signed main() {  
    Node *a = new Node(10);  
    Node *b = new Node(20);  
    Node *c = new Node(30);

    a->next = b;  
    b->prev = a;  
    b->next = c;  
    c->prev = b;  
}
```

---

### Conceptual Questions

- `void printList(Node *head) {}`
- `Node *insertBegin(Node *head) {}`
- `Node *insertEnd(Node *head) {}` // Teach Head and Tail Pointer
- `Node *deleteBegin(Node *head) {}`
- `Node *deleteEnd(Node *head) {}`
- `Node *insertPos(Node *head, int pos, int data) {}`

---

### Questions

#### Easy
- [Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/description/)
- [Middle of the Linked List](https://leetcode.com/problems/middle-of-the-linked-list/description/)
- [Palindrome Linked List](https://leetcode.com/problems/palindrome-linked-list/description/)
- [Remove Duplicates from Sorted List](https://leetcode.com/problems/remove-duplicates-from-sorted-list/description/)
- [Insert in a Sorted List](https://www.geeksforgeeks.org/problems/insert-in-a-sorted-list/1)
- [Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/description/)
- [Intersection of Two Linked Lists](https://leetcode.com/problems/intersection-of-two-linked-lists/description/)
- [Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/description/)

#### Medium
- [Linked List Cycle II](https://leetcode.com/problems/linked-list-cycle-ii/description/)
- [Remove Nth Node From End of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/description/)
- [Rotate List](https://leetcode.com/problems/rotate-list/description/)
- [Odd Even Linked List](https://leetcode.com/problems/odd-even-linked-list/description/)
- [Sort a Linked List of 0s, 1s and 2s](https://www.geeksforgeeks.org/problems/given-a-linked-list-of-0s-1s-and-2s-sort-it/1)
- [Swap Nodes in Pairs](https://leetcode.com/problems/swap-nodes-in-pairs/description/)
- [Remove Duplicates from Sorted List II](https://leetcode.com/problems/remove-duplicates-from-sorted-list-ii/description/)
- [Add Two Numbers](https://leetcode.com/problems/add-two-numbers/description/)
- [Flatten a Multilevel Doubly Linked List](https://leetcode.com/problems/flatten-a-multilevel-doubly-linked-list/description/)
- [Sort List (Use Merge Sort)](https://leetcode.com/problems/sort-list/description/)

#### Hard
- [Copy List with Random Pointer](https://leetcode.com/problems/copy-list-with-random-pointer/description/)
- [LRU Cache](https://leetcode.com/problems/lru-cache/description/)
- [Reverse Nodes in k-Group](https://leetcode.com/problems/reverse-nodes-in-k-group/description/)
- [LFU Cache](https://leetcode.com/problems/lfu-cache/description/)
