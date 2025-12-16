# Design Patterns

Design patterns are proven, reusable solutions to common problems in software design. They act as **blueprints**, not exact code you copy, helping you design systems that are **scalable, maintainable, and easy to modify**.

---

## What Is a Design Pattern?

A **design pattern** is a general, reusable solution to a commonly occurring problem in software design.

- It is **not** a complete, ready-to-use code snippet.
- It provides a **conceptual template** that you adapt to your program.
- Unlike algorithms, which give step-by-step instructions, design patterns describe **high-level approaches**.
- The same pattern can look different across languages, architectures, and codebases.

---

## Design Pattern vs Algorithm

| Aspect | Design Pattern | Algorithm |
|------|---------------|-----------|
| Purpose | Conceptual solution structure | Step-by-step problem-solving procedure |
| Level | High-level design | Low-level implementation |
| Outcome | System architecture / behavior | Final computed result |
| Analogy | Blueprint (flexible outline) | Recipe (exact steps) |

---

## Why Learn Design Patterns?

### 1. Proven, Reusable Solutions
- A toolkit of tried-and-tested solutions to recurring problems.
- Avoids reinventing the wheel.
- Teaches general problem-solving and design techniques.

### 2. Strengthens Object-Oriented Design
Design patterns demonstrate:
- Encapsulation
- Abstraction
- Polymorphism
- Delegation
- Composition  

They encourage thinking in terms of **architecture**, not just working code.

### 3. Improves Team Communication
- Provides a shared vocabulary.
- Phrases like *“Use a Singleton”* or *“Apply Strategy here”* convey intent quickly.
- Simplifies design discussions and code reviews.

### 4. Makes Code Easier to Understand
Many frameworks and libraries heavily use design patterns. Recognizing them helps you:
- Understand code faster
- Predict behavior
- Make safe changes and extensions

### 5. Develops System Design Skills
- Promotes scalable and reusable architecture.
- Helps design systems that grow without breaking.
- Shifts mindset from **coding** to **software design**.

---

## Classification of Design Patterns

### Creational Patterns
Focus on **object creation**, making systems flexible and reducing coupling.

### Structural Patterns
Focus on **how classes and objects are combined** into larger structures.

### Behavioral Patterns
Focus on **communication, workflows, and responsibility distribution** between objects.

---

## Creational Design Patterns

Creational patterns manage object creation, configuration, and representation, reducing dependency on concrete classes.

### List of Creational Patterns

- **Singleton**  
  Ensures a class has only one instance and provides global access to it.

- **Factory Method**  
  Defines an interface for creating objects but lets subclasses decide which class to instantiate.

- **Abstract Factory**  
  Provides an interface for creating families of related objects without specifying concrete classes.

- **Builder**  
  Constructs complex objects step-by-step, separating construction from representation.

- **Prototype**  
  Creates new objects by cloning existing ones instead of creating them from scratch.

### Creational Patterns — Summary

| Pattern | Purpose | When to Use |
|------|--------|-------------|
| Singleton | Guarantee a single instance | Shared resources (config, logger, DB connection) |
| Factory Method | Delegate object creation to subclasses | When class shouldn’t decide product type |
| Abstract Factory | Create families of related objects | UI themes, cross-platform systems |
| Builder | Step-by-step object construction | Objects with many optional parts |
| Prototype | Clone existing objects | When creation is expensive but copying is cheap |

---

## Structural Design Patterns

Structural patterns define how objects and classes are composed into larger systems while remaining flexible and efficient.

Common concerns:
- Composition vs inheritance
- Wrappers and adapters
- Object relationships
- Interface compatibility
- Efficient object sharing

### List of Structural Patterns

- **Adapter**  
  Converts one interface into another that a client expects.

- **Bridge**  
  Separates abstraction from implementation so both can evolve independently.

- **Composite**  
  Treats individual objects and object groups uniformly (tree structures).

- **Decorator**  
  Adds behavior dynamically to objects without modifying their class.

- **Facade**  
  Provides a simplified interface to a complex subsystem.

- **Flyweight**  
  Shares common state to reduce memory usage.

- **Proxy**  
  Controls access to another object (lazy loading, security, caching).

### Structural Patterns — Summary

| Pattern | Purpose | When to Use |
|------|--------|-------------|
| Adapter | Make incompatible interfaces work | Integrating legacy or third-party systems |
| Bridge | Separate abstraction from implementation | Multiple dimensions of variation |
| Composite | Uniform treatment of part-whole hierarchies | Trees (menus, UI, file systems) |
| Decorator | Add behavior dynamically | Avoid subclass explosion |
| Facade | Simplify complex subsystems | Hide system complexity |
| Flyweight | Share state to save memory | Large number of similar objects |
| Proxy | Control access to an object | Lazy loading, security, caching |

---

## Behavioral Design Patterns

Behavioral patterns define how objects interact and how responsibilities are distributed.

### List of Behavioral Patterns

- **Strategy**  
  Defines interchangeable algorithms selected at runtime.

- **Observer**  
  Notifies dependent objects when a subject changes state.

- **Command**  
  Encapsulates a request as an object (undo/redo, queuing).

- **Chain of Responsibility**  
  Passes a request along handlers until one processes it.

- **State**  
  Allows objects to change behavior when internal state changes.

- **Template Method**  
  Defines an algorithm skeleton with overridable steps.

- **Iterator**  
  Provides sequential access without exposing internal structure.

- **Mediator**  
  Centralizes complex communication between objects.

- **Memento**  
  Saves and restores an object’s internal state.

- **Visitor**  
  Adds operations without modifying object classes.

### Behavioral Patterns — Summary

| Pattern | Purpose | When to Use |
|------|--------|-------------|
| Strategy | Swap algorithms dynamically | Avoid conditionals for behavior |
| Observer | Notify multiple listeners | Event-driven systems |
| Command | Encapsulate actions | Undo/redo, task scheduling |
| Chain of Responsibility | Sequential request handling | Middleware, validation pipelines |
| State | Change behavior by state | Frequent behavior changes |
| Template Method | Algorithm reuse with variation | Framework base classes |
| Iterator | Traverse collections safely | Custom data structures |
| Mediator | Reduce direct object coupling | UI and communication systems |
| Memento | Save and restore state | Undo systems |
| Visitor | Add operations externally | Compilers, AST processing |

---

## Conclusion

Design patterns are not rules, but **tools**. Mastering them improves:
- Code quality
- System scalability
- Team collaboration
- Long-term maintainability  

They help you think like a **software architect**, not just a programmer.
