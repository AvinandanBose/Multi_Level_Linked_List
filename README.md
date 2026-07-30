
# 📌 Multi-Level Linked List

A comprehensive implementation and analysis of the **Multi-Level Linked List** data structure using **C/C++**, including detailed explanations of memory allocation, insertion operations, pointer manipulation, hierarchical traversal, and structural visualization. This repository is designed for students, educators, and developers who want to deeply understand how Multi-Level Linked Lists work internally.

---

# Repository Link

🔗Repository: [https://github.com/AvinandanBose/Multi_Level_Linked_List](https://github.com/AvinandanBose/Multi_Level_Linked_List)

---

## 📘 Introduction

A **Multi-level Linked List (MLL)** is an extension of the standard linked list in which each node contains two pointers instead of one.

Unlike ordinary linear lists, this hierarchical organization allows a linked list to represent complex relationships while maintaining the dynamic memory allocation properties of linked lists. A node in this structure consists of three parts:

* **Data**: Stores the information of the element.


* **Next Pointer**: Links a node to the next node in the same level.


* **Child Pointer**: Points to another linked list, thereby creating one or more additional levels of nodes.



Because of this organization, a Multi-level Linked List is capable of representing both linear and hierarchical relationships efficiently. It allows a node to become the starting point of another linked list, where each child list can itself contain nodes with child pointers, resulting in multiple levels of hierarchy. If a node does not have a child, its child pointer contains NULL, and likewise, the next pointer of the last node (tail) at each level points to NULL.

---

## 🚀 Key Advantages

* **Hierarchical Representation:** Efficiently models nested relationships natively, avoiding flat array-based workarounds.
* **Flexibility & Dynamism:** Irregular, "jagged" data (where sub-lists have completely different lengths) is handled gracefully.
* **Memory Efficient for Sparsity:** Child lists are created dynamically; nodes without children simply point to `NULL`, saving unused block memory.
* **Expandable:** New levels and sub-levels can be attached dynamically without needing to restructure or shift the existing hierarchy.
* **Recursive Synergy:** Pairs naturally with recursive algorithms to traverse deep hierarchies.

## ⚠️ Trade-offs & Disadvantages

* **Memory Overhead:** Each node requires memory for two pointers (`next` and `child`) instead of one, leading to a larger footprint.
* **Implementation Complexity:** Traversal, insertion, flattening, and deletion algorithms are more difficult and require careful pointer management or recursive stacks.
* **Lack of Random Access:** Reaching a deeply nested element requires sequential traversal across multiple levels and links.
* **Cache Inefficiency:** Because nodes are scattered randomly in heap memory, jumping between parents and children is generally cache-unfriendly.

## 🌍 Real-World Applications

* **File & Directory Systems:** Modeling OS directories containing files and sub-folders.
* **Nested UI Menus:** Multi-level drop-down menus in graphical user interfaces.
* **Document Object Models (DOM):** Representing nested HTML/XML tag hierarchies in browsers.
* **Categorization Trees:** Multi-tiered e-commerce catalogs and taxonomies.
* **Abstract Syntax Trees (ASTs):** Used by compilers for nested language constructs.
* **Organization Charts:** Mapping out corporate structures across managers and departments.

## ⚡ Complexity Analysis

### Time Complexity (Main List Operations)

| Operation | Best Case | Worst Case | Average Case |
| --- | --- | --- | --- |
| **Insert at Beginning** | $\Omega(1)$ | $O(1)$ | $\Theta(1)$ |
| **Insert at End** | $\Omega(1)$ | $O(n)$ | $\Theta(n)$ |
| **Insert at Position** | $\Omega(1)$ | $O(n)$ | $\Theta(n)$ |
| **Insert After Element** | $\Omega(1)$ | $O(n)$ | $\Theta(n)$ |
| **Delete at Beginning** | $\Omega(1)$ | $O(1)$ | $\Theta(1)$ |
| **Delete at End** | $\Omega(1)$ | $O(n)$ | $\Theta(n)$ |
| **Delete at Position** | $\Omega(1)$ | $O(n)$ | $\Theta(n)$ |

### Space Complexity

* **Auxiliary Space:** $O(1)$ for basic iterative operations (Insertion, Deletion). The algorithms use a constant number of temporary variables (`temp`, `newNode`, `toDelete`) regardless of the list size.
* **Holistic Space:** $O(n)$, representing the total memory required by the $n$ nodes in the entire data structure.

## 🛠️ Included Algorithms

This repository implements the following core algorithms:

1. **Creation & Allocation:** Safe dynamic memory allocation (`malloc`) with error handling.
2. **Insertion:** Adding nodes at the Beginning, End, specific Position, and conditionally linking as a `next` or `child` element relative to a target node.
3. **Deletion:** Safely removing nodes and freeing memory from the Beginning, End, and specific Positions.
4. **List Destruction:** A robust recursive algorithm (`destroyNodeRecursively`) that utilizes post-order style traversal to safely free all nodes in both the main lists and nested child lists, preventing memory leaks.

---
## 📚 Learning Outcomes

By studying and implementing the code in this repository, you will gain a deep understanding of advanced data structures and algorithmic analysis. Specifically, you will learn how to:

* **Model Hierarchical Data:** Understand how to transition from linear data models to complex, non-uniform hierarchical structures using multi-level nodes.
* **Master Advanced Pointer Manipulation:** Gain hands-on experience managing multiple pointers simultaneously (`next` for linear flow, `child` for depth) without losing track of references or causing segmentation faults.
* **Perform Rigorous Complexity Analysis:** 
  * **Time Complexity:** Learn how to mathematically derive Best ($\Omega$), Worst ($O$), and Average ($\Theta$) case time complexities using probability distributions and summation formulas.
  * **Space Complexity:** Understand the critical difference between *Auxiliary Space* (temporary memory used by the algorithm) and *Holistic/Full Data Input Space* (memory occupied by the entire data structure).
* **Handle Dynamic Memory Safely:** Learn the nuances of manual memory allocation using `malloc` and `free`, including how to safely calculate memory sizes based on pointer and data types (e.g., 20 bytes per node on 64-bit systems).
* **Implement Recursive Algorithms:** Discover how to effectively use recursion to process and destroy deeply nested structures, ensuring that sub-lists (child nodes) are completely freed before their parent nodes to prevent memory leaks.
* **Map Theory to Real-World Applications:** Recognize patterns where Multi-Level Linked Lists are the optimal choice, such as in operating system file directories, DOM trees, and UI routing.

----

# 👨‍💻 Author

Developed and analyzed by [@AvinandanBose](https://github.com/AvinandanBose)

---

# 📄 License

This project is licensed under the **MIT License**.

---

## ⭐ Support

If you found this helpful:

* ⭐ Star the repository
* 🍴 Fork it
* 📢 Share with others

---

<br>
<br>
<br>
