# Nested Typedef Structures in C

## Overview

This project demonstrates the use of **nested structures with `typedef` in C**. The program models a real-world scenario involving a dealership, a car, and its owner using multiple structures.

By combining nested structures with `typedef`, the code becomes more readable, organized, and easier to maintain.

---

## Concepts Covered

- Structures (`struct`)
- Nested structures
- `typedef` keyword
- Structure initialization
- Accessing nested members
- Formatted output using `printf()`

---

## Project Description

The program defines three structures:

### Owner

Stores owner details:

- First Name
- Last Name

### Car

Stores car details:

- Brand
- Manufacturing Year
- Owner Information

### Dealership

Stores dealership details:

- Dealership Name
- Featured Car Information

The `Dealership` structure contains a `Car`, and the `Car` structure contains an `Owner`, creating a nested hierarchy.

---

## Structure Definitions

```c
typedef struct {
    char firstName[20];
    char lastName[20];
} Owner;

typedef struct {
    char brand[30];
    int year;
    Owner owner;
} Car;

typedef struct {
    char name[30];
    Car featuredCar;
} Dealership;
```

---

## Structure Initialization

```c
Owner person = {"John", "Doe"};

Car car1 = {"Toyota", 2010, person};

Dealership d = {"City Motors", car1};
```

The program creates an owner, assigns that owner to a car, and then assigns the car to a dealership.

---

## Accessing Nested Members

```c
d.featuredCar.brand

d.featuredCar.year

d.featuredCar.owner.firstName

d.featuredCar.owner.lastName
```

Nested members are accessed using multiple dot (`.`) operators.

---

## Sample Output

```text
Dealership: City Motors
Featured Car: Toyota (2010), owned by John Doe
```

---

## Learning Outcomes

- Understanding nested structures in C
- Using `typedef` to simplify structure declarations
- Creating hierarchical data models
- Accessing deeply nested structure members
- Organizing related data efficiently

---

## Real-World Applications

- Vehicle Registration Systems
- Car Dealership Management Software
- Employee and Department Records
- Banking Applications
- Inventory Management Systems
- Embedded Systems Data Models

---

## Time Complexity

```text
O(1)
```

Accessing structure members takes constant time.

---

## Space Complexity

```text
O(1)
```

The program uses a fixed amount of memory for structure variables.

---

## Key Takeaway

Nested structures combined with `typedef` provide a clean and efficient way to represent real-world entities and their relationships, making C programs more structured and maintainable.

---

## Author

**Amrutha D N**
