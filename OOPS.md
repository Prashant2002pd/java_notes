
**_Inheritance_**

- Inheritance is a mechanism in Java that allows one class to inherit the properties and methods of another class. The class that inherits is called the subclass or child class, and the class being inherited from is called the superclass or parent class. Inheritance can help minimize code complexity and increase execution efficiency.

```java
class Animal {
  public void eat() {
    System.out.println("Animal is eating");
  }
}

class Dog extends Animal {
  public void bark() {
    System.out.println("Dog is barking");
  }
}

public class Main {
  public static void main(String[] args) {
    Dog dog = new Dog();
    dog.eat(); // Animal is eating
    dog.bark(); // Dog is barking
  }
}
```


***Encapsulation***

- Encapsulation in Java is the process of wrapping data and code together into a single unit, called a class. This bundling of data and methods makes it easier to create secure and reusable code.
- To encapsulate data in Java, you can declare the data as private. This means that the data can only be accessed by methods within the class. To access the data from outside the class, you can provide public getter and setter methods.

```java
private String name;

public String getName() {
  return name;
}

public void setName(String name) {
  this.name = name;
}
```

***Polymorphism***

- Polymorphism is a core concept of Object-Oriented Programming (OOP) that allows you to define one interface and have multiple implementations. This is achieved by method overloading and method overriding.
	-  Method Overloading
		Method overloading allows you to have multiple methods with the same name in the same class, but with different parameters. This allows you to perform the same action in different ways. For example, you could have a `calculateArea()` method that takes a `Rectangle` object as a parameter, and another `calculateArea()` method that takes a `Circle` object as a parameter.

	- Method Overriding
		Method overriding allows you to define a method in a subclass that has the same name and signature as a method in the superclass. When you call the method on an object of the subclass, the overridden method is called instead of the method in the superclass. This allows you to change the behavior of a method in a subclass without having to modify the superclass.

```java

class Animal {
  public void makeSound() {
    System.out.println("Animal sound");
  }
}

class Dog extends Animal {
  @Override
  public void makeSound() {
    System.out.println("Woof!");
  }
}

class Cat extends Animal {
  @Override
  public void makeSound() {
    System.out.println("Meow!");
  }
}

public class Main {
  public static void main(String[] args) {
    Animal animal = new Animal();
    animal.makeSound(); // Prints "Animal sound"

    Dog dog = new Dog();
    dog.makeSound(); // Prints "Woof!"

    Cat cat = new Cat();
    cat.makeSound(); // Prints "Meow!"
  }
}
```