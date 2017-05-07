# Java vs Swift: A Language Comparison Study
<!-- ## The battle of the Object Oriented overlords! -->

## 1. Language Purpose / Genesis
#### Java:
* To be portable and to operate in distributed environments
* To enable creation of applets for the World Wide Web
* Targeted for digital consumer devices and computers, predicted to rise in popularity at the time
* Created to replace [C](https://en.wikipedia.org/wiki/C_(programming_language)/[C++](https://en.wikipedia.org/wiki/C%2B%2B) for development, with better design

#### Swift:
* To be the best language for uses ranging from systems programming, to mobile and desktop apps, scaling up to cloud services
* Designed to make writing and maintaining correct programs easier for developers
* Built for the average programmer, and designed for coding even the simplest of mobile apps
* Created to replace [Objective-C](https://en.wikipedia.org/wiki/Objective-C) as the main development language for Apple platforms
----
### 2. Unique Features of the Language
### Java:
* Runs on [_Java Virtual Machine_](https://en.wikipedia.org/wiki/Java_virtual_machine) (JVM)
* Fully Object Oriented, i.e., object is at the outer most level of data structure in java. No stand alone methods, constants, and variables may exist outside of a class
* Objects are first-class types
* User-created types can only be reference-type

### Swift:
* Utilizes [_Low Level Virtual Machine_](https://en.wikipedia.org/wiki/LLVM) (LLVM) to compile and run
* Supports [Functional Programming Patterns](https://en.wikipedia.org/wiki/Functional_programming)
* Functions and closures are first-class types
* Closures unified with function pointers
* Supports tuples and multiple return values
* Supports creation of value types (structs) with methods, extensions, or protocols
* Supports type-inference

----
### 3. Namespaces
### Java:
* Explicit namespacing supported
* Namespacing is per-file
* A `package` is Java's mechanism for managing namespaces
* Access to any member methods or attributes inside a package is possible by invoking the package name before the member
* To create a package:
```java
package one.two.three;
// Class or inteface code inside
```
* To use a package:
```java
import one.two.three;    // Now we can access the package's members
```
* To access a specific class in a package:
```java
import java.io.File;    // Now we can type File instead of java.io.File
```


### Swift:
* Namespacing is implicit in Swift, all classes (etc) are implicitly scoped by the module they are in. Conflicting names can be resolved by prefixing the class name
* Namespacing is per-target (XCode module), and not per-file
* By default, current module takes precedence to implicitly resolve conflicts
* E.g:
```swift
var customController = UICollectionViewController() //your custom class
var uikitController = UIKit.UICollectionViewController() //class from UIKit
```
----
### 4. Types
### Java:
* The Primitive Data Types are all _value types_
* Both Reference and Primitive Data types are supported in Java
* Creation of new values types is **not** supported. Any new type can only be of _reference type_


1. Primitive Data Types:
  * byte
  * short
  * int
  * long
  * float
  * double
  * boolean
  * char
2. Reference Data Types:
  * Derived Data Types:
    * (arrays) (e.g: `int[]`, `char[]`, etc.)
  * User-defined Data Types:
    * Integer category data types:
      * Byte
      * Short
      * Int
      * Long
    * Character category data types:
      * Char
    * Float category data types
      * Float
      * Double
    * Boolean category data types
      * Boolean
    * (Custom types) (e.g: File, StreamBuffer, etc.)


### Swift:
* Named Types created using `struct` are all _value types_
* Both reference types and value types are supported in Swift
* New value types can be created using `struct` or `enum`


1. Named Types:
  * class (e.g: `Array`, `Dictionary`, `Set`, etc. )
  * struct (e.g: `Int`, `Double`, `String`, etc.)
  * enum (e.g: `Bit`, `Optional`, `Process`, etc.)
  * protocol (e.g: `Collection`, `Equatable`, etc.)
2. Compound Types:
  * Function Types <br />
    (E.g.)
    ```swift
    func someFunction(left: Int, right: Int) {}
    var f = someFunction // The type of f is (Int, Int) -> Void, not (left: Int, right: Int) -> Void.
    ```
  * Tuple Types <br />
    (E.g.)
      ```swift
      var someTuple = (top: 10, bottom: 12)  // someTuple is of type (top: Int, bottom: Int)
      ```
----
### 5. Classes
### Java:
* Classes can be defined in Java using the keyword `class`. For example:
```java
public class Dog {
   String breed;
   int age;
   String color;

   void barking() {
   }

   void hungry() {
   }

   void sleeping() {
   }
}
```
* New instances of the class are creating by usual variable declaration syntax, with the type as the class name. For example:
```java
Dog dogInstance = new Dog();
```

* Instances require a constructor. Every class has an implicit empty default constructor. Explicit default constructor or parameterized constructor can be defined if needed, using access specifier and class name. For example:
```java
public class Animal {
   String type;
   String color;

   // Explicit default constructor
   public Animal() {
     this.type = "Bird";
     this.color = "Blue";
   }

   // Explicit parameterized constructor
   public Animal(String type, String color) {
     this.type = type;
     this.color = color;
   }
}
```

* Java's _Garbage Collector_ requires a call to a class's destructor. Every class has an implicit destructor, which frees all states associated with the class. Explicit destructor can be defined if needed, using access specifier and the class name prefixed with a _tilde_ symbol (~). For example:
```java
public class Animal {
   String type;
   String color;

   // Destructor
   public ~Animal() {
     this.type = null;
     this.color = null;
   }
}
```

### Swift:
* Classes can be defined in Swift using the keyword `class`. For example:
```swift
public class Dog {
   var breed: String = "Lhasa Apso"
   var age: Int = 2
   var color: String = "White"

   func barking() {
   }

   func hungry() {
   }

   func sleeping() {
   }
}
```
* New instances of the class are creating by calling a class's initializer and letting a variable declaration infer the type. For example:
```swift
var dogInstance = Dog()
```

* Instances require an initializer. Every class has an implicit empty default initializer. Explicit default initializer or parameterized initializer can be defined if needed, using the function name `init`. For example:
```swift
public class Animal {
   var type: String
   var color: String

   // Explicit default initializer
   init() {
     self.type = "Bird"
     self.color = "Blue"
   }

   // Explicit parameterized initializer
   public Animal(type: String, color: String) {
     self.type = type
     self.color = color
   }
}
```

* A class's deinitializer ensures memory is freed after it's no longer needed. Every class has an implicit deinitializer, which frees all states associated with the class. Explicit deinitializer can be defined if needed, using the keyword `deinit`. For example:
```swift
public class Animal {
   var type: String?
   var color: String?

   // Deinitializer
   deinit() {
     self.type = nil
     self.color = nil
   }
}
```
----
### 6. Instance reference name in data type (_class_)
### Java:
An instance can refer to its own members using the keyword `this`. For example:
```java
public class Human {
  String name;

  public Human() {
    this.name = "Peter Griffin";  // "this" keyword used
  }
}
```

### Swift:
An instance can refer to its own members using the keyword `self`. For example:
```java
public class Human {
  var name: String

  init() {
    self.name = "Peter Griffin"  // "self" keyword used
  }
}
```
----
### 7. Properties
### Java:
* Java does not treat "Properties" any different from "Member variables"

* Private member variables in Java can only be accessed using getters and setters, if outside the scope of the class definition. The language does not have in-built support for default public getters and setters, and hence, require explicit declaration by the developer. For example:
```java
public class Human {
    private String name;

    // Getter
    public String getName() {
      return this.name;
    }

    // Setter
    public void setName(String name) {
      this.name = name;
    }
}
```

* "Backing Variables" and "Computed Properties" are not useful without a separate concept of "Properties", and hence, not applicable to Java


### Swift:
* A _Stored Property_ is a constant or variable that is stored as part of an instance of a particular class or structure. Stored properties can be either variable stored properties (introduced by the `var` keyword) or constant stored properties (introduced by the `let` keyword). For example:
```swift
struct FixedLengthRange {
    var firstValue: Int
    let length: Int
}
var rangeOfThreeItems = FixedLengthRange(firstValue: 0, length: 3)
rangeOfThreeItems.firstValue = 6
```

* A _Computed Property_ behaves syntactically like a variable, but does not actually require storage. Instead, accesses to the variable go through the getter and the setter. Thus, a computed variable is declared as a variable with a custom getter. For example:
```swift
struct Rect {
    var height: Int
    var maxY: Int { // maxY stores no value
      get {
        return y + height
      }
      set(newMaxY) {
        y = newMaxY - height
      }
    }
}
```

* Swift unifies the concept of "Property" and "Backing variable" into a single property declaration. i.e., a Swift property does not have a corresponding instance variable, and the backing store for a property is not accessed directly


----
### 8. Interfaces / Protocols
### Java:
* Java primarily supports polymorphism through _Interfaces_, and also allows classes to be bound to "contracts" using the same construct
* Java Interfaces are treated like a class, except they can only contain method signatures and fields
* They cannot contain any method implementation, but only the signature (name, parameters and exceptions) of the method
* Java Interfaces mandate declaration of all methods in the implementing class
* The declaration involves using the keyword `interface`. For example:
```java
public interface MyInterface {

    public String hello = "Hello";

    public void sayHello();
}
```
This can be implemented using the keyword `implements` on a class declaration. For example:
```java
public class MyClass implements MyInterface {

    // All of Interface's methods declared here
    public void sayHello() {
        System.out.println(MyInterface.hello);
    }
}
```
* The interface can be used by constructing an object of the conforming class. An interface cannot have its own instance. For example:
```java
MyInterface myInterface = new MyClass();
myInterface.sayHello();
```
* Java class can implement multiple interfaces. For example:
```java
public class MyClass implements MyInterface, MyOtherInterface {

    public void sayHello() {
        System.out.println("Hello");
    }

    public void sayGoodbye() {
        System.out.println("Goodbye");
    }
}
```
### Swift:
* Swift _Protocols_ are used in an identical manner as Java's Interfaces
* In Swift, a protocol can be adopted by a class, structure, or enumeration, to provide implementation of the required methods
* Protocol declaration involves using the keyword `protocol`. For example:
```swift
protocol MyProtocol {
    let hello = "Hello"
    var sayHello()
}
```
This can be implemented using the symbol `:` on a class declaration. For example:
```swift
public class MyClass : MyProtocol {
    func sayHello() {
      print(MyProtocol.hello)
    }
}
```
* The protocol can be used by initializing an object of the conforming class. A protocol cannot have its own instance. For example:
```swift
let myProtocol: MyProtocol = MyClass()
myProtocol.sayHello()
```
* The protocol doesn’t specify whether the property should be a stored property or a computed property—it only specifies the required property name and type. The protocol also specifies whether each property must be gettable or gettable and settable
* Swift allows a class to conform to multiple protocols if needed. For example:
```swift
public class MyClass : MyProtocol, MyOtherProtocol {

    func sayHello() {
      print("Hello")
    }

    func sayGoodbye() {
      print("Goodbye")
    }
}
```
----
### 9. Inheritance / Extension
### Java:
* Purely object oriented, i.e., no code construct may exist without a class.

### Swift:
----
### 10. Reflection
### Java:
* Purely object oriented, i.e., no code construct may exist without a class.

### Swift:
----
### 11. Memory management
### Java:
* Purely object oriented, i.e., no code construct may exist without a class.

### Swift:
----
### 12. Comparisons of references and values
### Java:
* Purely object oriented, i.e., no code construct may exist without a class.

### Swift:
----
### 13. Null/nil references
### Java:
* Purely object oriented, i.e., no code construct may exist without a class.

### Swift:
----
### 14. Errors and exception handling
### Java:
* Purely object oriented, i.e., no code construct may exist without a class.

### Swift:
----
### 15. Lambda expressions, closures, or functions as types
### Java:
* Purely object oriented, i.e., no code construct may exist without a class.

### Swift:
----
### 16. Implementation of _Listeners_ and _Event Handlers_
### Java:
* Purely object oriented, i.e., no code construct may exist without a class.

### Swift:
----
### 17. Singleton
### Java:
* Purely object oriented, i.e., no code construct may exist without a class.

### Swift:
----
### 18. Procedural Programming
### Java:
* Purely object oriented, i.e., no code construct may exist without a class.

### Swift:
----
### 19. Functional Programming
### Java:
* Purely object oriented, i.e., no code construct may exist without a class.

### Swift:
----
### 20. Multithreading
### Java:
* Purely object oriented, i.e., no code construct may exist without a class.

### Swift:
