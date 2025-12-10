#  Augmented Reality Object Placement System

This Python project simulates a **priority-driven AR object placement system** using core data structures like **AVL Trees** and **Min-Heaps**, implemented in a single file for simplicity.[web:1][web:2] The system allows users to add, update, manage, and render virtual objects in a 3D space while enforcing **collision avoidance** and **minimum distance constraints** through a menu-based CLI.[web:3][web:5]

---

##  Project Overview

This CLI-based simulation acts like the backend of an AR engine and handles:

- **Object Prioritization (Min-Heap):**  
  Renders or processes the most relevant objects first based on proximity, visibility, and interaction potential.
- **Spatial Management (AVL Tree):**  
  Stores and retrieves AR objects efficiently using unique IDs.
- **Collision Detection & Constraint Handling:**  
  Prevents overlapping objects and enforces minimum spatial distances.
- **Scene Rendering & Filtering:**  
  Lists and simulates rendering of objects in order of priority, with support for custom filtering logic.

All logic (heap, AVL tree, constraints, renderer, and menu) is contained in **one Python file**.


##  Data Structures Used

| Component              | Data Structure                        | Purpose                                               |
|------------------------|----------------------------------------|-------------------------------------------------------|
| Priority Queue         | MinHeap / MinHeapAR                   | Ensures lowest-priority value (highest importance) is processed first |
| Object Lookup          | AVL Tree                              | Fast search, insert, and delete based on object ID    |
| 3D Spatial Validation  | Bounding Box & Distance Calculations  | Avoids collisions and enforces placement rules        |


##  How to Run

### Prerequisites

- **Python 3.x** installed on your system.

### Run from terminal
```python ar_object_system.py```


The program will start an interactive **menu-driven interface** where you can add, update, and manage AR objects.


##  Features Covered in Menu

| Choice | Feature Description                                       |
|--------|-----------------------------------------------------------|
| 1      | Add AR object (priority-based)                           |
| 2      | Update object attributes or spatial constraints          |
| 3      | View object with highest priority                        |
| 4      | Search object by ID                                      |
| 5      | Remove AR object                                         |
| 6      | Display all AR objects in scene                          |
| 7      | Render AR objects in sorted priority                     |
| 8      | Add object with 3D position and constraints              |
| 9      | Detect collisions between two objects                    |
| 10     | Check if an object satisfies constraints                 |
| 11     | Exit the program                                         |


##  Algorithms in Use

- **MinHeap Insert & Remove:** \(O(\log n)\) time for maintaining priority queue operations.
- **AVL Tree Insert / Search / Delete:** \(O(\log n)\) due to self-balancing height. 
- **Collision & Constraint Checks:** \(O(n)\) over the number of objects in the scene.


##  Author

**Uhashini** – 3rd Year Engineering Student | Data Structures & AR Enthusiast  
This project was developed as part of a **Data Structures and Algorithms** focused exercise to combine theory (heaps, trees) with a practical AR-inspired use case.



