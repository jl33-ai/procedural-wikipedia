# Object-Oriented Programming 🖥️
_## Created by @jl33-ai 👦🏻 _

_Object-Oriented Programming (OOP) is one of the most effective approaches to writing software. In OOP, you write classes that represent real-world things, and you create objects based on these classes._

## Table of Contents 📝
- [Summary](#summary)
- [Key Concepts](#key-concepts)
  - [Abstraction](#abstraction)
  - [Encapsulation](#encapsulation)
  - [Inheritance](#inheritance)
  - [Polymorphism](#polymorphism)
- [Examples](#examples)
  

## Summary 📚
In object-oriented programming, **classes** 📚 and **objects** 🍏 are the two main aspects:

- **Classes** - Blueprint for creating objects (a particular data structure), providing initial values for states (member variables or attributes), and implementations of behavior (member functions or methods).
- **Objects** - An instance of a class.

## Key Concepts 💡

### Abstraction ⭐
Abstraction 🎭 means using simple things to represent complexity. We all know how to turn the TV 📺 on, but we don’t need to know how it works in order to enjoy it. In Java, abstraction is accomplished using Abstract Classes and Interfaces.

### Encapsulation 🗄️
Encapsulation is an OOP concept that binds together the data and functions that manipulate the data. It keeps both safe from outside interference and misuse. For example:

```java
public class Employee {
    // private data member  
    private String name;

    // getter method for name  
    public String getName() {
        return name;
    }  
    
    // setter method for name  
    public void setName(String name) {
        this.name=name;
    }  
} 
```
Here, the `name` data member is private, so it can only be accessed within the same class. No outside class can access the data member `name`. This is a great demonstration of encapsulation.

### Inheritance 🚗
Inheritance 👩‍👧 is a mechanism in which one object acquires all the properties and behaviours of a parent object. It’s an important part of OOPs (Object-Oriented programming system). For example:

```java
class Vehicle {
    // Vehicle class methods and fields
}

class Car extends Vehicle {
    // Car class methods and fields
}
```
Here, `Car` class _inherits_ the methods and fields of the `Vehicle` class.

### Polymorphism 💭
Polymorphism allows methods to be used in multiple ways depending on the context. The two main types are _method overloading_ and _method overriding_. For example:

```java
// Method Overloading
void func() { ... }
void func(int a) { ... }
void func(int a, int b) { ... }

// Method Overriding
class Base {
    void show() { ... }
}

class Derived extends Base {
    // This method overrides show() of parent
    void show() { ... }
}
```

## Examples 💻

1. **Creating a Class and Object in Java**

```java
class Fruit {
    String name;
    String color;
}

class Main {
    public static void main(String[] args) {

        // create an object of Fruit
        Fruit apple = new Fruit();

        // access fields and set values
        apple.name = "Apple";
        apple.color = "Red";

        System.out.println("Fruit Name: " + apple.name);
        System.out.println("Fruit Color: " + apple.color);
    }
}
```

2. **Inheritance in Java**

```java
// parent class
class Animal {
    void eat() {
        System.out.println("eating...");
    }
}

// child class
class Dog extends Animal {
    void bark() {
        System.out.println("barking...");
    }
}

// test class
class TestInheritance {
    public static void main(String args[]) {
        Dog d = new Dog();
        d.bark();
        d.eat();
    }
}
```

_Thanks for reading this OOP guide. Feel free to contribute! 😀_