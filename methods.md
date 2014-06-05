方法(Methods)
===============

>> Methods are functions that are associated with a particular type. Classes, structures, and enumerations can all define instance methods, which encapsulate specific tasks and functionality for working with an instance of a given type. Classes, structures, and enumerations can also define type methods, which are associated with the type itself. Type methods are similar to class methods in Objective-C.

方法是一些功能/函数的集合,这些功能/函数与某些特定类型相关联。类、结构体、枚举都可以定义实例方法；实例方法为指定类型的实例封装了特定的任务与功能。类、结构体、枚举也可以定义类(型)方法(type itself)；类型方法与类型自身相关联。类型方法与Objective-C中的类方法(class methods)相似。

>> The fact that structures and enumerations can define methods in Swift is a major difference from C and Objective-C. In Objective-C, classes are the only types that can define methods. In Swift, you can choose whether to define a class, structure, or enumeration, and still have the flexibility to define methods on the type you create.

在Swift中,结构体和枚举能够定义方法；事实上这是Swift与C/Objective-C的主要区别之一。在Objective-C中,类是唯一能定义方法的类型。在Swift中，你能够选择是否定义一个类/结构体/枚举，并且你仍然享有在你创建的类型(类/结构体/枚举)上定义方法的灵活性。

### 实例方法(Instance Methods) ###
>> Instance methods are functions that belong to instances of a particular class, structure, or enumeration. They support the functionality of those instances, either by providing ways to access and modify instance properties, or by providing functionality related to the instance’s purpose. Instance methods have exactly the same syntax as functions, as described in Functions.

实例方法是某个特定类、结构体或者枚举类型的实例的方法。实例方法支撑实例的功能: 或者提供方法,以访问和修改实例属性;或者提供与实例的目的相关的功能。实例方法的语法与函数完全一致，参考函数说明(a link should be here)。

>> You write an instance method within the opening and closing braces of the type it belongs to. An instance method has implicit access to all other instance methods and properties of that type. An instance method can be called only on a specific instance of the type it belongs to. It cannot be called in isolation without an existing instance.

实例方法要写在它所属的类型的前后括号之间。实例方法能够访问他所属类型的所有的其他实例方法和属性。实例方法只能被它所属的类的特定实例调用。实例方法不能被孤立于现存的实例而被调用。

>> Here’s an example that defines a simple Counter class, which can be used to count the number of times an action occurs:

下面是定义一个很简单的类Counter的例子(Counter能被用来对一个动作发生的次数进行计数):

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

>> The Counter class defines three instance methods:
>> • increment increments the counter by 1.
>> • incrementBy(amount: Int) increments the counter by an specified integer amount.
>> • reset resets the counter to zero.

Counter类定理了三个实例方法：
- increment让计数器按一递增；
- incrementBy(amount: Int)让计数器按一个指定的整数值递增；
- reset将计数器重置为0。

>> The Counter class also declares a variable property, count, to keep track of the current counter value.

Counter这个类还声明了一个可变属性count，用它来保持对当前计数器值的追踪。

>> You call instance methods with the same dot syntax as properties:

和调用属性一样，用点语法(dot syntax)调用实例方法:

```
1| let counter = Counter()
2| // the initial counter value is 0
3| counter.increment()
4| // the counter's value is now 1
5| counter.incrementBy(5)
6| // the counter's value is now 6
7| counter.reset()
8| // the counter's value is now 0
```

### 方法的局部和外部参数名称(Local and External Parameter Names for Methods) ###
