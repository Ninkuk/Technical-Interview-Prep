#technical 

## Overview
- 

---
## Building Blocks of OOP

### Classes
- user-defined data types
- blueprint or template for objects
- has constructors to initialize
- things can be overloaded

```java
class Car {
	// attributes
	private String make;
	private String model;
	private int year;
	
	// methods
	
	// constructors (are technically methods)
	public Car() {} // no arg constructor
	public Car(String make, String model, int year) {
		this.make = make;
		this.model = model;
		this.year = year;
	}
}
```

### Objects
- instances of classes with specific data

```java
Car myCar = new Car("Mazda", "MX-5", 2021);
```

### Attributes
- variables defined inside a class
- usually set with constructor or setters

### Methods
- functions stated inside a class
- most common are getters and setters
- technically constructors are also methods that are executed automatically when the object is formed

---
## Encapsulation
- this is the concept of getters and setters
- hides the data from users - safer access

```java
// setter
public void setMake(String make) {
	this.make = make;
}

// getter
public String getMake() {
	return this.make;
}
```

---
## Inheritance (`extends`)
- create a new class from an existing class
- use `final` to disable inheritance from a class
- you can only inherit from 1 parent (unlike interface)

```java
class Animal { public int legs; }

class Dog extends Animal { public String furColor; }
// Dog has both legs and furColor

class Human extends Animal { public int SSN; }
// Human has legs and SSN but not fur
```

---
## Polymorphism

We can achieve polymorphism using the following ways (see end of notes):
1. Method Overriding
2. Method Overloading
3. Operator Overloading

---
## Abstraction (`implements`)
- Two ways to achieve abstraction: abstract class & interface

![](https://www.csharpstar.com/wp-content/uploads/2016/02/Abstract-Class.jpg?2d1e51&2d1e51)

### Abstract Class
- this uses `extends`
- cannot be instantiated because there is incomplete implementation
- abstract class provides partial abstraction - some things can be implemented in the parent

```java
abstract class Animal {
	// animal sounds is not implemented
	public abstract void animalSound();
	
	// sleep is implemented
	public void sleep() {
		System.out.println("zzz");
	}
}

class Dog extends Animal {
	public void animalSound() {
	    System.out.println("The dog says: woof woof");
	}
}
```

### Interface
- a class can implement multiple interfaces (but not inherit >1)
- interface provides full abstraction - nothing can be implemented in the parent

```java
interface Animal {
  public void animalSound(); // interface method (does not have a body)
  public void run(); // interface method (does not have a body)
}

class Dog implements Animal {
	public void animalSound() {
	    System.out.println("The dog says: woof woof");
	}
	
	public void sleep() {
	    System.out.println("zzz");
	}
}
```

---
## Other Concepts

### Method Overloading
- same name, different params
	- different number of parameters, different types of parameters, or both

```java
public int sum(int num1, int num2) {...}
public int sum(int num1, int num2, int num3) {...}
```

### Method Overriding
- Use `@Override` annotation
- Use `super` keyword to access the method of the parent from the child
- Remember: `toString` - Overrides from Class Class

### Operator Overloading