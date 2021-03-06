TypeScript是JavaScript的一个超集，主要提供对类型系统和ES6的支持。

## Type

Type annotations

布尔值是最基础的数据类型。

        let  isDone: boolean = false;
        
As in JavaScript, all numbers in TypeScript are floating point values.

浮点数

These floating point numbers get the type `number`.
        
        let decimal: number = 6;
        
Another fundamental part of creating programs in JavaScript for webpages and servers alike is working with textual data.

在TS中，any是一种新添加的类型，即在JS中原本并不存在。

任意值(any)用来表示变量可以被赋值为任意类型。

        let myFavoriteNumber: string =  'seven';
        myFavoriteNumber = 7;
        
这段代码会报错。

非any类型的变量在赋值过程中是不允许改变类型的。

        let myFavoriteNumber : any = 'seven';
        myFavoriteNumber = 7;
        
这段代码可以正常运行。

如果没有明确的指定类型，那么TypeScript会依照类型推论(Type Inference)的规则推断出一个类型。

以下代码虽然没有指定类型，但是会在编译的时候报错：

        let myFavoriteNumber =  'seven';
        myFavoriteNumber = 7;
        
TypeScript, like JavaScript, allows you to work with arrays of values.

Array types can be written in one of two ways.

In the first, you use the type

        let arr: number[] = [0, 1, 1, 2, 4, 8];

那么，我们是否依旧可以像JS中一样不对数组中元素的类型进行限制？

## Tuple

Tuple types allow you to express an array where the type of a fixed is known, but need 
        
数组合并了相同类型的对象，而元组(Tuple)合并了不同类型的对象。

        let person: [string, number];
        
        person = ["bill", 26];
        
 
## Interface

接口可以用于对**对象的形状(Shape)** 进行描述。

        interface Person {

## Class

使用`class`关键字定义类，使用`constructor`定义构造函数。

        class Person {
            public  name: string;
            public  constructor(name: string) {
                this.name = name;
            }
            
            public sayHi (): string {
                return `My name is ${this.name}`
            }
        }
        
TypeScript有三种可以使用的访问修饰符(Access Modifiers)，分别是`public`,`private`和`protected`。        

- `public`修饰的属性或方法是公有的，
        
For instance, C# requires that each member be explicitly labeled `public` to be visible.

In TypeScript, each member is `public` by default.

`abstract`关键字用于定义抽象类和其中的抽象方法。

## Decorator

装饰器的本质是函数。

## Function 

We can add types to each of the parameters and then to the function itself to add a return type.

So if the function does not return a value, you would use `void` instead of leaving it off.