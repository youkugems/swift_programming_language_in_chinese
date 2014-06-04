方法(Methods)
===============

>> Methods are functions that are associated with a particular type. Classes, structures, and enumerations can all define instance methods, which encapsulate specific tasks and functionality for working with an instance of a given type. Classes, structures, and enumerations can also define type methods, which are associated with the type itself. Type methods are similar to class methods in Objective-C.

方法是一些功能/函数的集合,这些功能/函数与某些特定类型相关联。类、结构体、枚举都可以定义实例方法；实例方法为指定类型的实例封装了特定的任务与功能。类、结构体、枚举也可以定义类(型)方法(type itself)；类型方法与类型自身相关联。类型方法与Objective-C中的类方法(class methods)相似。

>> The fact that structures and enumerations can define methods in Swift is a major difference from C and Objective-C. In Objective-C, classes are the only types that can define methods. In Swift, you can choose whether to define a class, structure, or enumeration, and still have the flexibility to define methods on the type you create.

在Swift中,结构体和枚举能够定义方法；事实上这是Swift与C/Objective-C的主要区别之一。在Objective-C中,类是唯一能定义方法的类型。在Swift中，你能够选择是否定义一个类/结构体/枚举，并且你仍然享有在你创建的类型(类/结构体/枚举)上定义方法的灵活性。

实例方法(Instance Methods)
====
>> Instance methods are functions that belong to instances of a particular class, structure, or enumeration. They support the functionality of those instances, either by providing ways to access and modify instance properties, or by providing functionality related to the instance’s purpose. Instance methods have exactly the same syntax as functions, as described in Functions.

实例方法是某个特定类、结构体或者枚举类型的实例的方法。实例方法支撑实例的功能: 或者提供方法,以访问和修改实例属性;或者提供与实例的目的相关的功能。实例方法的语法与函数完全一致，参考函数说明(a link should be here)。

You write an instance method within the opening and closing braces of the type it belongs to. An instance method has implicit access to all other instance methods and properties of that type. An instance method can be called only on a specific instance of the type it belongs to. It cannot be called in isolation without an existing instance.

Here’s an example that defines a simple Counter class, which can be used to count the number of times an action occurs:

```
1|  class Counter {
2|   var count = 0
3|   func increment() {
4|     count++
5|   }
6|   func incrementBy(amount: Int) {
7|     count += amount
8|   }
9|   func reset() {
10|    count = 0
11|  }
12|}
```

and so on...


方法的局部和外部参数名称(Local and External Parameter Names for Methods)
====
