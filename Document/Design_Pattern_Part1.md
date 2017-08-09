## 主要内容 ##
> #### 常用设计模式 ####
> #### 面向对象设计原则 ####

## 正文 ##
### 1. *常用*设计模式 ###
虽然**GoF设计模式**只有23个，但是它们各具特色，每个模式都为某一个可重复的设计问题提供
了一套解决方案。根据它们的用途，设计模式可分为**创建型(Creational)，结构型(Structural)和行为型(Behavioral)**三种。
+ **创建型模式**主要用于描述如何创建对象
+ **结构型模式**主要用于描述如何实现类或对象的组合
+ **行为型模式**主要用于描述类或对象怎样交互以及怎样分配职责

在GoF 23种设计模式中包含5种创建型设计模式、7种结构型设计模式和11种行为型设计模式。此外，根据某个模式主要是用于处理类之间的关系还是对象之间的关系，设计模式还可以分为类模式和对象模式。我们经常将两种分类方式结合使用，如单例模式是对象创建型模式，模板方法模式是类行为型模式。


| 类型                          | 模式名称                                    | 学习难度 | 使用频率 | 是否完成 |
| ----------------------------- | ------------------------------------------- | -------- | -------- | -------- |
| 创建者模式-Creational Pattern | [单例模式-Singleton Pattern][1]             | ★☆☆☆☆    | ★★★★☆    | [x]      |
| 创建者模式-Creational Pattern | [工厂方法模式-Factory Method Pattern][2]    | ★★☆☆☆    | ★★★★★    | [x]      |
| 创建者模式-Creational Pattern | [抽象工厂模式-Abstract Factory Pattern][3]  | ★★★★☆    | ★★★★★    | [x]      |
| 创建者模式-Creational Pattern | 原型模式-Prototype Pattern                  | ★★★☆☆    | ★★★☆☆    | [ ]      |
| 创建者模式-Creational Pattern | 建造者模式-Builder Pattern                  | ★★★★☆    | ★★☆☆☆    | [ ]      |
| 结构型模式-Structural Pattern | [适配器模式-Adapter Pattern][4]             | ★★☆☆☆    | ★★★★☆    | [x]      |
| 结构型模式-Structural Pattern | 桥接模式-Bridge Pattern                     | ★★★☆☆    | ★★★☆☆    | [ ]      |
| 结构型模式-Structural Pattern | [组合模式-Composite Pattern][5]             | ★★★☆☆    | ★★★★☆    | [x]      |
| 结构型模式-Structural Pattern | 装饰模式-Decorator  Pattern                 | ★★★☆☆    | ★★★☆☆    | [ ]      |
| 结构型模式-Structural Pattern | [外观模式-Façade  Pattern][6]               | ★☆☆☆☆    | ★★★★★    | [x]      |
| 结构型模式-Structural Pattern | 享元模式-Flyweight  Pattern                 | ★★★★☆    | ★☆☆☆☆    | [ ]      |
| 结构型模式-Structural Pattern | [代理模式-Proxy  Pattern][7]                | ★★★☆☆    | ★★★★☆    | [ ]      |
| 行为型模式                    | 职责链模式-Chain  of Responsibility Pattern | ★★★☆☆    | ★★☆☆☆    | [ ]      |
| 行为型模式                    | [命令模式-Command  Pattern][8]              | ★★★☆☆    | ★★★★☆    | [ ]      |
| 行为型模式                    | [解释器模式-Interpreter  Pattern][12]             | ★★★★★    | ★☆☆☆☆    | [ ]      |
| 行为型模式                    | [迭代器模式-Iterator  Pattern][9]                | ★★★☆☆    | ★★★★★    | [ ]      |
| 行为型模式                    | 中介者模式-Mediator  Pattern                | ★★★☆☆    | ★★☆☆☆    | [ ]      |
| 行为型模式                    | 备忘录模式-Memento  Pattern                 | ★★☆☆☆    | ★★☆☆☆    | [ ]      |
| 行为型模式                    | [观察者模式-Observer  Pattern][10]                | ★★★☆☆    | ★★★★★    | [ ]      |
| 行为型模式                    | 状态模式-State  Pattern                     | ★★★☆☆    | ★★★☆☆    | [ ]      |
| 行为型模式                    | [策略模式-Strategy  Pattern][11]                 | ★☆☆☆☆    | ★★★★☆    | [ ]      |
| 行为型模式                    | 模板方法模式-Template  Method Pattern       | ★★☆☆☆    | ★★★☆☆    | [ ]      |
| 行为型模式                    | 访问者模式-Visitor  Pattern                 | ★★★★☆    | ★☆☆☆☆    | [ ]      |

[1]: https://github.com/gregecho/JavaDesignPattern/blob/master/Document/Design_Pattern_Part2_Creational_Pattern_Singleton_Pattern.md
[2]: https://github.com/gregecho/JavaDesignPattern/blob/master/Document/Design_Pattern_Part2_Creational_Pattern_Factory_Pattern.md
[3]: https://github.com/gregecho/JavaDesignPattern/blob/master/Document/Design_Pattern_Part2_Creational_Pattern_Factory_Pattern.md
[4]: https://github.com/gregecho/JavaDesignPattern/blob/master/Document/Design_Pattern_Part3_Structural_Pattern_Adapter_Pattern.md
[5]: https://github.com/gregecho/JavaDesignPattern/blob/master/Document/Design_Pattern_Part3_Structural_Pattern_Composite_Pattern.md
[6]: https://github.com/gregecho/JavaDesignPattern/blob/master/Document/Design_Pattern_Part3_Structural_Pattern_Facade_Pattern.md
[7]: https://github.com/gregecho/JavaDesignPattern/blob/master/Document/Design_Pattern_Part3_Structural_Pattern_Proxy_Pattern.md
[8]: https://github.com/gregecho/JavaDesignPattern/blob/master/Document/Design_Pattern_Part4_Behavioral_Pattern_Command_Pattern.md
[9]: https://github.com/gregecho/JavaDesignPattern/blob/master/Document/Design_Pattern_Part4_Behavioral_Pattern_Iterator_Pattern.md
[10]: https://github.com/gregecho/JavaDesignPattern/blob/master/Document/Design_Pattern_Part4_Behavioral_Pattern_Observer_Pattern.md
[11]: https://github.com/gregecho/JavaDesignPattern/blob/master/Document/Design_Pattern_Part4_Behavioral_Pattern_Strategy_Pattern.md
[12]:https://github.com/gregecho/JavaDesignPattern/blob/master/Document/Design_Pattern_Part4_Behavioral_Pattern_Interpreter_Pattern.md

### 2. 面向对象设计原则 ###

**面向对象设计原则**为支持可维护性复用而诞生，这些原则蕴含在很多设计模式中，它们是从许多设计方案中总结出的指导性原则。面向对象设计原则也是我们用于评价一个设计模式的使用效果的重要指标之一。

| 设计原则名称                                        | 定义                                             | 使用频率 |
| --------------------------------------------------- | ------------------------------------------------ | -------- |
| 单一职责原则 (Single Responsibility Principle, SRP) | 一个类只负责一个功能领域中的相应职责             | ★★★★☆    |
| 开闭原则 (Open-Closed Principle, OCP)               | 软件实体应对扩展开放，而对修改关闭               | ★★★★★    |
| 里氏代换原则 (Liskov Substitution Principle, LSP)   | 所有引用基类对象的地方能够透明地使用其子类的对象 | ★★★★★    |
| 依赖倒转原则 (Dependence Inversion Principle, DIP)  | 抽象不应该依赖于细节，细节应该依赖于抽象         | ★★★★★    |
| 接口隔离原则 (Interface Segregation Principle, ISP) | 使用多个专门的接口，而不使用单一的总接口         | ★★☆☆☆    |
| 合成复用原则 (Composite Reuse Principle, CRP)       | 尽量使用对象组合，而不是继承来达到复用的目的     | ★★★★☆    |
| 迪米特法则 (Law of Demeter, LoD)                    | 一个软件实体应当尽可能少地与其他实体发生相互作用 | ★★★☆☆    |

#### 2.1 单一职责原则 ####
> **定义**单一职责原则(Single Responsibility Principle, SRP)：一个类只负责一个功能领域中的相应职责，或者可以定义为：就一个类而言，应该只有一个引起它变化的原因。
>> 在软件系统中，一个类（大到模块，小到方法）承担的职责越多，它被复用的可能性就越小，而且一个类承担的职责过多，就相当于将这些职责耦合在一，当其中一个职责变化时，可能会影响其他职责的运作，因此要将这些职责进行分离，将不同的职责封装在不同的类中，即将不同的变化原因封装在不同的类中，如果多个职责总是同时发生改变则可将它们封装在同一类中。

#### 2.2 开放封闭原则 ####
> **定义**开闭原则(Open-Closed Principle, OCP)：一个软件实体应当对扩展开放，对修改关闭。即软件实体应尽量在不修改原有代码的情况下进行扩展。

> 在开闭原则的定义中，软件实体可以指一个软件模块、一个由多个类组成的局部结构或一个独立的类。


#### 2.3 里氏替换原则 ####
> 里氏代换原则是实现开闭原则的重要方式之一，由于使用基类对象的地方都可以使用子类对象，因此在程序中尽量使用基类类型来对对象进行定义，而在运行时再确定其子类类型，用子类对象来替换父类对象。

在使用里氏代换原则时需要注意如下几个问题：
>+ 子类的所有方法必须在父类中声明，或子类必须实现父类中声明的所有方法。根据里氏代换原则，为了保证系统的扩展性，在程序中通常使用父类来进行定义，如果一个方法只存在子类中，在父类中不提供相应的声明，则无法在以父类定义的对象中使用该方法。
>+ 我们在运用里氏代换原则时，尽量把父类设计为抽象类或者接口，让子类继承父类或实现父接口，并实现在父类中声明的方法，运行时，子类实例替换父类实例，我们可以很方便地扩展系统的功能，同时无须修改原有子类的代码，增加新的功能可以通过增加一个新的子类来实现。里氏代换原则是开闭原则的具体实现手段之一。


#### 2.3 依赖倒置原则 ####
如果说开闭原则是面向对象设计的目标的话，那么**依赖倒转原则就是面向对象设计的主要实现机制之一**，它是系统抽象化的具体实现。
>+ 依赖倒转原则(Dependency Inversion Principle, DIP)：抽象不应该依赖于细节，细节应当依赖于抽象。换言之，要针对接口编程，而不是针对实现编程。
>+ 依赖倒转原则要求我们在程序代码中传递参数时或在关联关系中，尽量引用层次高的抽象层类，即*使用接口和抽象类进行变量类型声明、参数类型声明、方法返回类型声明，以及数据类型的转换*等，而不要用具体类来做这些事情。为了确保该原则的应用，一个具体类应当只实现接口或抽象类中声明过的方法，而不要给出多余的方法，否则将无法调用到在子类中增加的新方法。

#### 2.4 接口隔离原则 ####
> **接口隔离原则(Interface Segregation Principle, ISP)**：使用多个专门的接口，而不使用单一的总接口，即客户端不应该依赖那些它不需要的接口。

根据接口隔离原则，当一个接口太大时，我们需要将它分割成一些更细小的接口，使用该接口的客户端仅需知道与之相关的方法即可。每一个接口应该承担一种相对独立的角色，不干不该干的事，该干的事都要干。

#### 2.5 组合复用原则 ####
> 合成复用原则(Composite Reuse Principle, CRP)：尽量使用对象组合，而不是继承来达到复用的目的。

>+ 在面向对象设计中，可以通过两种方法在不同的环境中复用已有的设计和实现，即通过组合/聚合关系或通过继承，但首先应该考虑使用组合/聚合，组合/聚合可以使系统更加灵活，降低类与类之间的耦合度，一个类的变化对其他类造成的影响相对较少；其次才考虑继承，在使用继承时，需要严格遵循里氏代换原则，有效使用继承会有助于对问题的理解，降低复杂度，而滥用继承反而会增加系统构建和维护的难度以及系统的复杂度，因此需要慎重使用继承复用。
>+ 一般而言，如果两个类之间是“Has-A”的关系应使用组合或聚合，如果是“Is-A”关系可使用继承。"Is-A"是严格的分类学意义上的定义，意思是一个类是另一个类的"一种"；而"Has-A"则不同，它表示某一个角色具有某一项责任。

