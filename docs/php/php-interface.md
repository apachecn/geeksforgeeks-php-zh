# PHP|接口

> Original: [https://www.geeksforgeeks.org/php-interface/](https://www.geeksforgeeks.org/php-interface/)

接口允许用户创建程序，指定类必须实现的公共方法，而不涉及特定方法如何实现的复杂性和细节。 它通常被称为下一级抽象。 它类似于抽象方法，类似于抽象类。 接口的定义就像定义类一样，但是使用 interface 关键字和函数原型替换 class 关键字。 该接口不包含任何数据变量。 该接口很有帮助，因为它确保为程序员希望使用的所有方法维护一种元数据。

**创建接口**

以下是如何使用*interface*关键字定义接口的示例。

```php
<?php 

interface MyInterfaceName {
   public  function methodA();
   public  function methodB();
} 

?>
```

接口的几个特征包括：

*   接口由没有实现的方法组成，这意味着接口方法是抽象方法。
*   接口中的所有方法都必须具有公共可见性范围。
*   接口与类不同，因为类只能从一个类继承，而类可以实现一个或多个接口。

要实现接口，请使用**实现**运算符，如下所示：

```php
<?php

class MyClassName implements MyInterfaceName{
   public  function methodA() { 

     // method A implementation
   } 
   public  function methodB(){ 

     // method B implementation
   } 
}

?>
```

**具体类**：实现接口的类称为具体类。 它必须实现接口中定义的所有方法。 由于歧义错误，无法实现同名接口。 与任何类一样，可以使用**扩展**运算符扩展接口，如下所示：

```php
<?php 

interface MyInterfaceName1{

    public  function methodA();

}

interface MyInterfaceName2 extends MyInterfaceName1{

    public  function methodB();
}

?>
```

**示例**：

```php
<?php 

interface MyInterfaceName{

    public function method1();
    public function method2();

}

class MyClassName implements MyInterfaceName{

    public function method1(){
        echo "Method1 Called" . "\n";
    }

    public function method2(){
        echo "Method2 Called". "\n";
    }
} 

$obj = new MyClassName;
$obj->method1();
$obj->method2();

?>
```

**Output:**

```php
Method1 Called
Method2 Called

```

**PHP 接口的优点**

*   接口允许不相关的类实现相同的方法集，而不考虑它们在类继承层次结构中的位置。
*   一个接口可以对多个继承建模，因为一个类可以实现多个接口，而它只能扩展一个类。
*   继承的实现将使调用者不必完全实现对象方法，而只关注对象接口，因此调用者接口不受影响。