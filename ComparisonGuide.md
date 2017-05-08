<p align="center">
  <img align="center" src="http://www.myiconfinder.com/uploads/iconsets/128-128-0148ab901cc8f25c9d7d25f6656b1297-java.png" alt="java">
  <b>VS</b>
<img align="center" src="https://cdn4.iconfinder.com/data/icons/logos-3/1300/swift-seeklogo-128.png" alt="swift">
</p>

# Java vs Swift: A Language Comparison Study

## 1. Language Purpose / Genesis
#### Java:
* To be portable and to operate in distributed environments
* To enable creation of applets for the World Wide Web
* Targeted for digital consumer devices and computers, predicted to rise in popularity at the time
* Created to replace [C](https://en.wikipedia.org/wiki/C_(programming_language))/[C++](https://en.wikipedia.org/wiki/C%2B%2B) for development, with better design

#### Swift:
* To be the best language for uses ranging from systems programming, to mobile and desktop apps, scaling up to cloud services
* Designed to make writing and maintaining correct programs easier for developers
* Built for the average programmer, and designed for coding even the simplest of mobile apps
* Created to replace [Objective-C](https://en.wikipedia.org/wiki/Objective-C) as the main development language for Apple platforms
----
### 2. Unique Features of the Language
#### Java:
* Runs on [_Java Virtual Machine_](https://en.wikipedia.org/wiki/Java_virtual_machine) (JVM)
* Fully Object Oriented, i.e., object is at the outer most level of data structure in java. No stand alone methods, constants, and variables may exist outside of a class
* Objects are first-class types
* User-created types can only be reference-type

#### Swift:
* Utilizes [_Low Level Virtual Machine_](https://en.wikipedia.org/wiki/LLVM) (LLVM) to compile and run
* Supports [Functional Programming Patterns](https://en.wikipedia.org/wiki/Functional_programming)
* Functions and closures are first-class types
* Closures unified with function pointers
* Supports tuples and multiple return values
* Supports creation of value types (structs) with methods, extensions, or protocols
* Supports type-inference

----
### 3. Namespaces
#### Java:
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

#### Swift:
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
#### Java:
* The Primitive Data Types are all _value types_
* Both Reference and Primitive Data types are supported in Java
* Creation of new values types is **not** supported. Any new type can only be of _reference type_
* Broadly, there's two categories of data types, as follows:
    1. **Primitive Data Types**:
        * byte
        * short
        * int
        * long
        * float
        * double
        * boolean
        * char
    2. **Reference Data Types**:
        * **Derived Data Types**:
            * (arrays) (e.g: `int[]`, `char[]`, etc.)
        * **User-defined Data Types**:
            * Integer category data types:
                * Byte
                * Short
                * Int
                * Long
            * **Character category data types**:
                * Char
            * **Float category data types**:
                * Float
                * Double
            * **Boolean category data types**:
                * Boolean
            * **(Custom types)** (e.g: File, StreamBuffer, etc.)


#### Swift:
* Named Types created using `struct` are all _value types_
* Both reference types and value types are supported in Swift
* New value types can be created using `struct` or `enum`
* Swift categorizes data types in two major forms, as shown below:
    1. **Named Types**:
        * class (e.g: `Array`, `Dictionary`, `Set`, etc. )
        * struct (e.g: `Int`, `Double`, `String`, etc.)
        * enum (e.g: `Bit`, `Optional`, `Process`, etc.)
        * protocol (e.g: `Collection`, `Equatable`, etc.)
    2. **Compound Types**:
        * **Function Types** <br />
        (E.g.)
            ```swift
            func someFunction(left: Int, right: Int) {}
            var f = someFunction // The type of f is (Int, Int) -> Void, not (left: Int, right: Int) -> Void.
            ```
        * **Tuple Types** <br />
        (E.g.)
            ```swift
            var someTuple = (top: 10, bottom: 12)  // someTuple is of type (top: Int, bottom: Int)
            ```
----
### 5. Classes
#### Java:
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

#### Swift:
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
       init(type: String, color: String) {
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
#### Java:
An instance can refer to its own members using the keyword `this`. For example:
```java
public class Human {
  String name;

  public Human() {
    this.name = "Peter Griffin";  // "this" keyword used
  }
}
```

#### Swift:
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
#### Java:
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

#### Swift:
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
#### Java:
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

#### Swift:
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
#### Java:
* Java allows a class to inherit from a single superclass (single inheritance)
* The methods declared in the superclass can be overriden in the derived class using the annotation `@Override`
* A class can inherit from a superclass using the keyword `extends`. For example:
    ```java
    class Super {
        public void superMethod() {
            // stuff done here
        }
    }

    class Sub extends Super {
        @Override
        public void superMethod() {
            super.superMethod();
            // Some extra stuff done here instead
        }
    }
    ```
* A class cannot be extended directly in java after declaration

#### Swift:
* Swift supports single inheritance
* The methods declared in the base class can be overridden using the keyword `override`
* A class can inherit from a base class using the symbol `:`. For example:
    ```swift
    class SomeSuperclass {
        func superMethod() {
            // stuff done here
        }
    }

    class SomeSubclass: SomeSuperclass {
        override func superMethod() {
            // Some extra stuff done here
            super.superMethod()
        }
    }
    ```
* Swift allows adding functionality to existing classes, structs, enumerations, and protocols, including core library constructs, using _Extensions_
* Extensions are declared using keyword `extension`. For example:
    ```swift
    extension Double {
        var km: Double { return self * 1_000.0 }
        var m: Double { return self }
        var cm: Double { return self / 100.0 }
        var mm: Double { return self / 1_000.0 }
        var ft: Double { return self / 3.28084 }

        func newMethod() {
            // Performs additional functions
        }
    }
    ```
* Extensions can provide additional initializers, methods, and computed properties
----
### 10. Reflection
#### Java:
* The required classes for java reflection are provided under `java.lang.reflect` package
* Under java reflection API, we can invoke methods at runtime irrespective of the access specifier used with them
* Reflection can be used to get information about:
  * **Class**: The `getClass()` method is used to get the name of the class to which an object belongs
      ```java
      Dog dog = new Dog();
      Class dogClass = dog.getClass();
      ```
  * **Constructors**: The `getConstructors()` method is used to get the public constructors of the class to which an object belongs
      ```java
      dogConstructor = dog.getClass().getConstructor();
      ```
  * **Methods**: The `getMethods()` method is used to get the public methods of the class to which an object belongs
      ```java
      Method[] dogMethods = dogClass.getMethods();
      ```
  * **Fields**: The `getFields()` method is used to get the public fields of the class to which an object belongs
      ```java
      Field[] dogFields = dogClass.getFields();
      ```
* And many other pieces of information can be obtained, including _superclass_, _canonicalName_, _annotations_, etc.

#### Swift:
* Swift supports runtime inspection of code through reflection
* Swift's reflection capabilities are based around a `struct` called _Mirror_. You create a mirror for a particular `subject` and the mirror will then let you query it
* _Reflecting initializers_ can be used to easily create a mirror. For example:
    ```swift
    public init(reflecting subject: Any)  // The type of the subject is Any
    ```
* A mirror instance can be obtained as follows:
    ```swift
    // Bookmark declaration
    public struct Bookmark {
       enum Group {
          case Tech
          case News
       }
       let title: String?
       let keywords: [String]
       let group: Group
    }
    let aBookmark = Bookmark(title: "Appventure", keywords: ["Swift", "iOS", "OSX"], group: .Tech)

    // Mirror creation for bookmark instance
    let aMirror = Mirror(reflecting: aBookmark)
    print(aMirror)  // prints : Mirror for Bookmark
    ```
* The Mirror struct contains several types to help identify the information you'd like to query. This includes:
  * DisplayStyle
      ```swift
      public enum DisplayStyle {
        case Struct
        case Class
        case Enum
        case Tuple
        case Optional
        case Collection
        case Dictionary
        case Set
      }
      ```
  * AncestorRepresentation
* Mirror instance can be used to perform reflection in many ways. The available properties / methods on a Mirror include the following:
  * `children`
      ```swift
      let children: Children
      ```
      This can be used as:
      ```swift
      for case let (label?, value) in aMirror.children {
        print (label, value)
      }
      //prints:
      //: title Optional("Appventure")
      //: keywords ["Swift", "iOS", "OSX"]
      //: group Tech
      ```
  * `displayStyle`
      ```swift
      displayStyle: Mirror.DisplayStyle?
      ```
      This can be used as:
      ```swift
      print (aMirror.displayStyle)
      // prints: Optional(Swift.Mirror.DisplayStyle.Struct)
      ```
  * `subjectType`
      ```swift
      let subjectType: Any.Type
      ```
      This can be used as:
      ```swift
      print(aMirror.subjectType)
      //prints : Bookmark
      print(Mirror(reflecting: 5).subjectType)
      //prints : Int
      print(Mirror(reflecting: "test").subjectType)
      //prints : String
      ```
  * `superclassMirror`
      ```swift
      func superclassMirror() -> Mirror?
      ```
      This can be used as:
      ```swift
      print(Mirror(reflecting: aBookmark).superclassMirror())
      // prints: nil
      // try a class
      print(Mirror(reflecting: aBookmark.store).superclassMirror())
      // prints: Optional(Mirror for Store)
      ```
----
### 11. Memory management
#### Java:
* Java does not allow manual memory management. Instead, it relies on its own **Garbage Collection** (GC) mechanism. Java Garbage Collection is the process to identify and remove the unused objects from the memory and free space to be allocated to objects created in the future processing
* Basic Garbage Collection involves 3 steps:
  * **Marking**
  * **Normal Deletion**
  * **Deletion with Compacting**
* JVM Heap Memory is physically divided into two parts:
  * **Young Generation**: All new objects are created in this generation. When this generation is filled up, _Minor GC_ kicks in
  * **Old Generation**: Contains the objects that are long lived and survived after many rounds of Minor GC. Garbage Collection is performed in Old Generation memory when it’s full. Old Generation Garbage Collection is called _Major GC_ and usually takes longer time
* Java provides a lot of memory switches that can be used to set the memory sizes and their ratios. For example:
  * -Xms
  * -Xmx
  * -XX:MaxPermGen, etc.

#### Swift:
* Memory management in Swift is handled automatically by **Automatic Reference Counting** (ARC). Whenever a variable holds an instance of a class, the memory count for that object increases by 1. If the variable goes out of scope or gets set to nil, the memory count decreases by 1
* ARC keeps track of _Reference Cycles_ to manage memory. Strong References increment or decrement the reference count, while _Weak_ and _Unowned References_ do not
* Reference cycles can cause memory leaks, and can be avoided by declaring leak-causing variables as `weak` or `unowned`, depending on the use

----
### 12. Comparisons of references and values
#### Java:
* Value types can be directly compared using the `==` operator. For example:
    ```java
    int a = 10;
    int b = 20;
    if (a == b) { // is FALSE
        // do stuff
    }
    ```
* Reference types have two ways of comparison:
  * _Comparing the references_: The `==` operator can be used to check if two objects are holding the same reference
  * _Comparing the values held by the references_: The `.equals()` method is used to check whether two references both refer to the same value
    ```java
    String a = "Hey";
    String b = "Hey";
    if (a == b) { // is FALSE
        // References compared
    }
    if (a.equals(b)) { // is TRUE
        // values compared
    }

    String c = b;
    if (c == b) { // is TRUE
        // References compared
    }
    if (c.equals(b)) { // is TRUE
        // values compared
    }
    ```

#### Swift:
* All types' values can be compared using the `==` operator. For example:
    ```swift
    let a = 10
    let b = 10
    if a == b { // is TRUE
        // do stuff
    }

    let fighter = "300"
    let movie = "300"
    if movie == fighter { // string comparison. Found TRUE
        // do stuff
    }
    ```
* Reference equality can be checked using a `===` operator. For example:
    ``` swift
    let era = movie
    if era === movie { // is TRUE
        // do stuff
    }
    ```
----
### 13. Null/nil references
#### Java:
* In Java, `null` keyword is used as a special value to signify:
  * Uninitialized state
  * Termination condition
  * Non-existing object
  * An unknown value
* Java does not implicitly check for null references. Instead, the developer has the responsibility to implements ways to handle null references. For example:
    ```java
    String hey;
    List<String> stringList;
    if (stringList == null) {
        stringList = new ArrayList<>();
    } else if (hey != null) {
        stringList.add(hey);
    }
    ```

#### Swift:
* Swift uses the keyword `nil` to denote the absence of a value of a certain type
* The language provides a construct to manage `nil`, using the `Optional` _enumeration_. A data type can never be assigned nil unless it is an optional. An optional type has the symbol `?` suffixed to an existing type. For example:
    ```swift
    var hey: String?  // String optional
    let there = "What's up!"  // NOT AN OPTIONAL
    hey = there
    if let hey = hey {  // Similar to checking (hey != nil). The first hey is a new String variable, while the second one is String optional
        print(hey)  // hey is assured to have a value
    }
    ```
* Swift `Optional` allows a few other handy features, such as:
  * **Optional Chaining**: Access a variable or method only if no `nil` types hindering access:
      ```swift
      var name: String? = "Stewie"
      print(name?.append("Griffin"))
      var someInstance: SomeClass? = SomeClass()
      someInstance?.someMember?.someNestedMember?.someNestedValue
      ```
  * **Nil Coelescing**: Used to provide a default value if unwrapping an optional fails. This is implemented using the `??` operator:
      ```swift
      let firstName: String?
      var anotherName = firstName ?? "Meg"  // if firstName is nil, "Meg" is assigned to anotherName
      ```
----
### 14. Errors and exception handling
#### Java:
* Java identifies three categories of Exceptions:
  * **Checked Exceptions**: An exception that occurs at the compile time; also called as _Compile-time Exceptions_. These exceptions cannot simply be ignored at the time of compilation. The programmer needs to take care of (handle) these exceptions. For example:
    ```java
    public static void main(String args[]) {		
        File file = new File("E://file.txt");
        FileReader fr = new FileReader(file); // Exception can occur here. Compiler finds this, hence compilation error
    }
    ```
  * **Unchecked Exceptions**: An exception that occurs at the time of execution. Also called as _Runtime Exceptions_. These include programming bugs, such as logic errors or improper use of an API. Runtime exceptions are ignored at the time of compilation. For example:
    ```java
    public static void main(String args[]) {
        int num[] = {1, 2, 3, 4};
        System.out.println(num[5]); // Execution fails due to ArrayIndexOutOfBoundsException exception
    }
    ```
  * **Errors**: These are not exceptions at all, but problems that arise beyond the control of the user or the programmer. Errors are typically ignored in the code because there is rarely that can be done about an error. For example, if a stack overflow occurs, an error will arise. They are also ignored at the time of compilation.
* A method can catch an exception using `try` and `catch` block. A `finally` block is executed whether an exception occurs or not:
    ```java
    public static void main(String args[]) {
        try {
            int a[] = new int[2];
            a[3] = 10;
        } catch(ArrayIndexOutOfBoundsException e) {
            System.out.println(e.printStackTrace());
        } finally {
            System.out.println("Done");
        }
    }
    ```
* If a method does not handle a checked exception, the method must declare it using the `throws` keyword. The `throws` keyword appears at the end of a method's signature
* `throws` is used to postpone the handling of a checked exception, while `throw` is used to invoke an exception explicitly. For example:
    ```java
    public void deposit(double amount) throws RemoteException {
        // Method implementation
        throw new RemoteException();
    }
    ```
* Java can implement _Automatic Resource Management_ using `try-with-resources`. The created resource is closed automatically at the end of the block. To use a class with try-with-resources statement it should implement `AutoCloseable` interface and the `close()` method of it gets invoked automatically at runtime. For example:
    ```java
    public static void main(String args[]) {
        try(FileReader fr = new FileReader("E://file.txt")) {
            char[] a = new char[50];
            fr.read(a);   // reads the content to the array
            for(char c : a)
            System.out.print(c);   // prints the characters one by one
        } catch(IOException e) {
            e.printStackTrace();
        }
    }
    ```

#### Swift:
* In Swift, errors are represented by values of types that conform to the `Error` protocol. This empty protocol indicates that a type can be used for error handling.
* Any function can be allowed to safely fail by throwing errors. For example:
    ```swift
    struct PurchasedSnack {
        let name: String
        init(name: String, vendingMachine: VendingMachine) throws {
            try vendingMachine.vend(itemNamed: name)
            self.name = name
        }
    }
    ```
* A `do-catch` statement is commonly used to handle errors by running a block of code. If an error is thrown by the code in the `do` clause, it is matched against the `catch` clauses to determine which one of them can handle the error. For example:
    ```swift
    do {
        try buy(fruits: 2, veg: 3)
    } catch Purchase.noMoney {
        print("Oops, out of money!")
    } catch Store.noStock {
        print("Oops, items out of stock!")
    }
    ```
* Unlike most languages, error handling in Swift does **not** involve unwinding the call stack, a process that can be computationally expensive
----
### 15. Lambda expressions, closures, or functions as types
#### Java:
* Lambda expressions are a new construct in Java, supported in Java 8+. They are implemented using _Functional Interfaces_ (Interfaces annotated with `@FunctionalInterface`, containing only one abstract method)
* Java 8 has a new package, `java.util.function`, that contains a number of commonly used functional interfaces
* In Java, the lambda expressions could be bound to variables of different types. For example:
    ```java
    // Function<T, R> is a FunctionalInterface under java.util.function package
    Function<Integer,Integer> add1 = x -> x + 1;
    Function<String,String> concat = x -> x + 1;

    Integer two = add1.apply(1); //yields 2
    String answer = concat1.apply("0 + 1 = "); //yields "0 + 1 = 1"
    ```
* Java 8+ has support for _Method References_ to create same functions as lambda expressions. For example:
    ```java
    public class Utils {
        public static Integer add1(Integer x) { return x + 1; }
        public static String concat1(String x) { return x + 1; }
    }

    Function<Integer,Integer> add1 = Utils::add1;   // add1 holds a method reference to Utils::add1
    Function<String,String> concat1 = Utils::concat1; // concat1 holds a method reference to Utils::concat1
    ```

#### Swift:
* Swift supports self-contained chunks of code that can be passed around and used, called _Closures_. Closures can capture and store references to any constants and variables from the context in which they are defined. This is known as closing over those constants and variables. For example:
    ```swift
    // a closure that take one Int and return an Int
    var double: (Int) -> (Int) = { x in
        return x * 2
    }

    double(2) // 4
    ```
* There are three kinds of closures in Swift:
    * **Global Functions**: They have a name and cannot capture any values
    * **Nested Functions**: They have a name and can capture values from their enclosing functions
    * **Closure Expressions**: They don’t have a name and can capture values from their context
* Closures can be received as a parameter by functions. For example:
    ```swift
    var numbers = [1, 4, 2, 5, 8, 3]

    // sort(by:) takes a closure as a parameter
    numbers.sort(by: { x, y in
        return x < y
    })
    ```
* Every function has a specific **function type**, made up of the parameter types and the return type of the function. For example:
    ```swift
    func addTwoInts(_ a: Int, _ b: Int) -> Int {
        return a + b
    }
    ```
    The type of this function is `(Int, Int) -> Int`
*  A function type can also be used as the return type of another function. For example:
    ```swift
    // This function returns a function of type (Int) -> Int
    func chooseStepFunction(backward: Bool) -> (Int) -> Int {
        return backward ? stepBackward : stepForward
    }
    ```
----
### 16. Implementation of _Listeners_ and _Event Handlers_
#### Java:
* There are three pieces to this construct in Java:
    * **The Component**: Generates events. An event is a component's way of letting a listener know that something has happened.
    * **The Event Class**: Holds all of the information necessary for a listener to figure out what happened.
    * **The Listener Interface**: An interface that defines the methods used by a component to dispatch events
* A Listener, which must implement the `ActionListener` interface and register itself with a trigger component (e.g.: Button). `ActionEvent` includes methods for learning an action's command string, modifiers, and identification string
* E.g: Event handling for a button press:
    ```java
    public class Beeper ... implements ActionListener {
        ...
        //where initialization occurs
        button.addActionListener(this);
        ...
        public void actionPerformed(ActionEvent e) {
            ...//Make a beep sound...
        }
    }
    ```

#### Swift:
* Triggers and Events can be handled in multiple ways under Swift:
    * **KVO**: _Key-Value-Observing_ is a capability inherited from the language predecessor, Objective-C. KVO features come with the class `NSObject`, which can be inherited to provide the KVO capabilities. Any property which is to be observed needs to be marked as `dynamic`. For example:
        ```swift
        class Car: NSObject {
            dynamic var miles = 0
            dynamic var name = "Turbo"
        }

        class CarObserver: NSObject {
            private var kvoContext: UInt8 = 1

            private let car: Car

            init(_ car: Car) {
                self.car = car
                super.init()
                car.addObserver(self, forKeyPath: "miles",
                options: NSKeyValueObservingOptions.New, context: &kvoContext)
            }
        }

        override func observeValueForKeyPath(keyPath: String,
            ofObject object: AnyObject, change: [NSObject : AnyObject],
            context: UnsafeMutablePointer<Void>) {
            if context == &kvoContext {
            println("Change at keyPath = \(keyPath) for \(object)")
            }
        }

        deinit {
            car.removeObserver(self, forKeyPath: "miles")
        }
        ```
        KVOs are only supported for Objective-C types, i.e., no structs, enums, and no generics.

    * **Observable Objects**: An object can be made observable by having its type adopt the `PropertyObservable` protocol. For example:
        ```swift
        enum CarProperty {
            case Miles, Name
        }

        class Car: PropertyObservable {
            typealias PropertyType = CarProperty
            let propertyChanged = Event<CarProperty>()

            dynamic var miles: Int = 0 {
                didSet {
                    propertyChanged.raise(.Miles)
                }
            }

            dynamic var name: String = "Turbo" {
                didSet {
                    propertyChanged.raise(.Name)
                }
            }
        }
        ```
        Whenever a property changes, the didSet ‘internal’ property observer is used to raise the event. The above can be used as follows:
        ```swift
        func viewDidLoad() {
            var car = Car();
            car.propertyChanged.addHandler(self, handler: ViewController.onPropertyChanged)
            car.miles = 34
        }

        func onPropertyChanged(property: CarProperty) {
            println("A car property changed!")
        }
        ```
    * **Observable Properties**: Notification of changes can be handled by the properties themselves, for example:
        ```swift
        class Observable<T> {
            let didChange = Event<(T, T)>()
            private var value: T

            init(_ initialValue: T) {
                value = initialValue
            }

            func set(newValue: T) {
                let oldValue = value
                value = newValue
                didChange.raise(oldValue, newValue)
            }

            func get() -> T {
                return value
            }
        }
        ```
        This can be used as follows:
        ```swift
        class Car {
            let miles = Observable<Int>(0)
            let name = Observable<String>("Turbo")
        }

        func viewDidLoad() {
            var car = Car();
            car.name.didChange.addHandler(self, handler: ViewController.nameDidChange)
            car.name.set("Speedy")
            println("The car is now called \(car.name.get())")
        }

        func nameDidChange(oldValue: String, newValue: String) {
            println("Name changed from \(oldValue) to \(newValue)")
        }
        ```
* Better ways of handling events exist using **delegation pattern**, implemented as shown below:
    ```swift
    // Delegate protocol: Provides blueprint
    protocol RatingPickerDelegate {
        func didSelectRating(picker: RatingPicker, rating: Int)
    }

    // Delegator: Asks to do something
    class RatingPicker {
        weak var delegate: RatingPickerDelegate?
        init(withDelegate delegate: RatingPickerDelegate?) {
            self.delegate = delegate
        }
        func selectRating(selectedRating: Int) {
            delegate?.didSelectRating(picker: self, rating: selectedRating)
        }
    }

    // Delegate: Does something when asked by Delegator
    class RatingPickerHandler: RatingPickerDelegate {
        let ratingPicker = RatingPicker()
        ratingPicker.delegate = self
        func didSelectRating(picker: RatingPicker, rating: Int) {
            // do something in response to a rating being selected
        }
    }
    ```
* Another possible way is by using `NSNotification`, a subclass of `NSObject`
* Swift's Interface Builder can be used to directly connect view `Outlets` to view `Actions`
----
### 17. Singleton
#### Java:
Singleton can be implemented in a few different ways, including **thread-unsafe** and **eager** ways. Preferred way of implementing **thread-safe** and **lazy initialization** is supported and needs careful design. One of the best implementations has been given by Bill Pugh, as shown below:
```java
public class Singleton {
    private Singleton(){}

    private static class SingletonHelper {
        private static final Singleton INSTANCE = new Singleton();
    }

    public static Singleton getInstance() {
        return SingletonHelper.INSTANCE;
    }
}
```
The `private inner static class` that contains the instance of the singleton class does not get loaded into memory until someone calls the `getInstance()` method to create the `Singleton` class instance. Hence, initialization is lazy. In addition, it does not require synchronization, and is able to be thread-safe.

#### Swift:
Since Swift 3, singletons can be easily made thread-safe and lazily initialized. For example:
```swift
class SomeManager {
    static let sharedInstance = SomeManager()
}

// To use it
SomeManager.sharedInstance
```
As of Swift 1.2, all global variables are instantiated lazily. Hence, the `sharedInstance` is only created when `SomeManager` instance is required. As stated in Apple's [Swift Blog](https://developer.apple.com/swift/blog/?id=7)
> “The lazy initializer for a global variable (also for static members of structs and enums) is run the first time that global is accessed, and is launched as `dispatch_once` to make sure that the initialization is atomic. This enables a cool way to use `dispatch_once` in your code: just declare a global variable with an initializer and mark it private.”
----
### 18. Procedural Programming
#### Java:
* Java was not created with Procedural Programming paradigm in mind, but it is loosely possible to follow certain design patterns to make it look so
* If really needed, one naive way of programming procedurally in Java would be by placing all instructions in the `main` function
* Procedural programming can be mapped onto object-oriented programming, by using a single _default object_ to interpret all procedure calls, contain all _global variables_, and mapping procedure calls to messages to this _default object_. In this sense, any object-oriented programming could contains procedural programming

#### Swift:
* Swift is more open towards multiple language paradigms than Java. Hence, procedural programming is supported, especially since elements can exist outside the scope of classes
* All instructions can be placed in one function, allowing a programming style very closely resempling procedural paradigm
----
### 19. Functional Programming
#### Java:
* Similar to Procedural paradigm suppot, it is loosely possible to emulate Functional Programming paradigm in Java
* Using Java 8's _lambda expressions_ and _anonymous functions_ facilitates writing programs in this paradigm. For instance, functions can be stored as objects using Functional Interfaces. Details can be found in [Section 15](https://github.com/gokussjx/Bm346_OOLanguageComparison/blob/master/ComparisonGuide.md#java-14)
* Java has many derivative languages, including a popular functional language **[Scala](https://www.scala-lang.org/)** (Scalable Language)

#### Swift:
* Swift natively supports functional programming
* Programs can be written in Swift using fully functional design
* As mentioned in [Section 15](https://github.com/gokussjx/Bm346_OOLanguageComparison/blob/master/ComparisonGuide.md#swift-14), Swift is additionally able to write programs using just constructs such as closures, function types, etc. This can result in functional programming
----
### 20. Multithreading
#### Java:
* Java is a multi-threaded programming language. There's two major ways of creating multi-threaded programs in Java:
    * **Create a Thread by Implementing a Runnable Interface**: The `Runnable` interface defines a single method, `run()`, meant to contain the code executed in the thread. The `Runnable` object is passed to the `Thread` constructor, as in the `HelloRunnable` example:
        ```java
        public class HelloRunnable implements Runnable {
            public void run() {
                System.out.println("Hello from a thread!");
            }

            public static void main(String args[]) {
                (new Thread(new HelloRunnable())).start();
            }
        }
        ```
        The thread is started by calling the `start()` function on a newly created thread
    * **Create a Thread by Extending a Thread Class**: The `Thread` class itself implements `Runnable`, though its run method does nothing. An application can subclass `Thread`, providing its own implementation of run, as in the `HelloThread` example:
        ```java
        public class HelloThread extends Thread {
            public void run() {
                System.out.println("Hello from a thread!");
            }

            public static void main(String args[]) {
                (new HelloThread()).start();
            }
        }
        ```
* Multitasking can be achieved by letting multiple threads start or run in parallel
* Under Java's JavaFX framework, multitasking can be achieved using `Platform.runLater()`, or by using `Task` class

#### Swift:
* Swift supports concurrency using **Grand Central Dispatch** (GCD). It provides three main types of queues:
    * **Main queue**: runs on the main thread and is a serial queue
    * **Global queue**: concurrent queues that are shared by the whole system. There exist 4 such queues with different priorities: {_high, default, low, background_}
    * **Custom queue**: queues that can be created by a developer which can be serial or concurrent
* With GCD, tasks can be dispatched in two ways:
    * **Synchronously**: Function returns control to the caller after the task is completed
    * **Asynchronously**: Function returns immediately, ordering the task to be done but not waiting for it. Hence, _non-blocking_ parallel execution
* Swift supports multitasking, including by dispatching tasks asynchronously
