
# Lecture 2 : OOPS (Abstraction & Encapsulation)

---

## 1. Why Did We Move Beyond Procedural Programming?

### 1.1 Early Languages

**1. Machine Language (Binary)**
- Direct CPU instructions in 0s & 1s.
- **Drawbacks**:
  - Extremely error-prone: one bit flip breaks the program.
  - Tedious to write and maintain.
  - No abstraction—every detail is manual.

**2. Assembly Language**
- Introduced mnemonics (e.g. `MOV A, 61h`) instead of raw bits.
- Still hardware-tied: code changes with CPU architecture.
- Scalability: remains very limited for large systems.

### 1.2 Procedural (Structured) Programming

- **Features Introduced**:
  - Functions for code reuse
  - Control structures: if-else, switch, for/while loops
  - Blocks for grouping statements

- **Advantages**:
  - Improved readability over assembly.
  - Modularized small to mid-size programs.

- **Limitations**:
  - Poor real-world mapping: Difficult to model complex entities.
  - Data security gaps: No built-in access control—everything is globally visible.
  - Reusability & scalability issues.

---

## 2. Entering Object-Oriented Programming

- **Core Idea**: Model your application as interacting objects mirroring real-world entities.
- **Benefits**:
  - Natural mapping of domain concepts (User, Car, Ride).
  - Secure data encapsulation—control access.
  - Code reuse via inheritance and interfaces.
  - Scalability through loosely coupled modules.

---

## 3. Modeling Real-World Entities in Code

### 3.1 Objects, Classes, & Instances

- **Object**: A real-world “thing” with attributes and behaviors.
- **Class**: Blueprint defining those attributes (fields) and behaviors (methods).
- **Instance**: Concrete object in memory, created via the class.

---

## 4. Deep Dive: Pillar 1 – Abstraction

**Definition**:  
Abstraction hides unnecessary implementation details and exposes only what is essential.

### 4.1 Real-World Analogies

- **Driving a Car**: You interact with the interface, not internal mechanisms.
- **Using a TV or Laptop**: Interfaces hide thousands of low-level operations.

### 4.2 Language-Level Abstraction

- **Control Structures**: High-level constructs (`if`, `for`) abstract machine-level instructions.

---

## 5. Code-Based Abstraction: Abstract Classes & Interfaces

### 5.1 Abstract Class Example (C++)

```cpp
// Abstract interface for any Car type
class Car {
public:
  virtual void startEngine() = 0;
  virtual void shiftGear(int newGear) = 0;
  virtual void accelerate() = 0;
  virtual void brake() = 0;
  virtual ~Car() {}
};
```

- **Key Points**:
  - Declares required operations.
  - Hides implementation.
  - Promotes polymorphism.

### 5.2 Concrete Subclass Example
(See actual code section)

---

## 6. Benefits of Abstraction

1. Simplified Interfaces
2. Ease of Maintenance
3. Code Reuse
4. Reduced Complexity

---

## 7. Deep Dive: Pillar 2 – Encapsulation

**Definition**:  
Encapsulation bundles data and methods into a single unit and restricts access to inner workings.

### 7.1 Two Facets of Encapsulation

1. **Logical Grouping**  
   - Example: `Car` class encapsulates `engineOn`, `accelerate()`, etc.

2. **Data Security**  
   - Restricts direct access.
   - Example: View odometer, but can't reset it.

### 7.2 Real-World Analogies

- **Medicine Capsule**: Contains both data and protective layer.
- **Car Odometer**: Read-only via interface.

### 7.3 Access Modifiers in C++

- `public`: Accessible everywhere.
- `private`: Accessible only within class.
- `protected`: Accessible in class and its subclasses.

### 7.4 Getters & Setters with Validation

Allows controlled and validated access to private fields.

---

## 7.5 Encapsulation Benefits

1. Robustness  
2. Maintainability  
3. Clear Contracts  
4. Modularity
