# PHP 中的静态函数

> 原文:[https://www.geeksforgeeks.org/static-function-in-php/](https://www.geeksforgeeks.org/static-function-in-php/)

在某些情况下，根据类而不是对象来访问方法和属性非常方便。这可以借助**静态**关键字来完成。任何声明为静态的方法都可以在不创建对象的情况下访问。静态函数与类相关联，而不是类的实例。他们只被允许访问静态方法和静态变量。要向类中添加静态方法，需要使用 static 关键字。

```php
public static function test()
{
    // Method implementation
}

```

可以通过使用范围解析运算符(::)在类外部直接调用它们，如下所示:

```php
MyClass::test();

```

**示例:**此示例将静态函数说明为计数器。

```php
<?php
/* Use static function as a counter */

class solution {

    static $count;

    public static function getCount() {
        return self::$count++;
    }
}

solution::$count = 1;

for($i = 0; $i < 5; ++$i) {
    echo 'The next value is: '. 
    solution::getCount() . "\n";
}

?>
```

**Output:**

```php
The next value is: 1
The next value is: 2
The next value is: 3
The next value is: 4
The next value is: 5

```

**什么时候定义静态方法？**
static 关键字用于类的所有对象共有的变量和方法的上下文中。因此，任何可以在一个类的多个实例之间共享的逻辑都应该被提取并放入静态方法中。PHP 静态方法最常用于包含静态方法的类，这些静态方法通常只被称为像 Laravel 和 CakePHP 这样的 PHP 框架的实用类。

下面是展示静态方法使用的 PHP 代码。

**示例:**这个示例说明了 PHP 中的静态方法。

```php
<?php
/* Use of static method in PHP */

class A {

    public function test($var = "Hello World") {
        $this->var = $var;
        return $this->var;
    }
}

class B {
    public static function test($var) {
        $var = "This is static";
        return $var;
    }
}

// Creating Object of class A
$obj = new A();

echo $obj->test('This is non-static'); 
echo "\n";
echo B::test('This is non-static'); 

?>
```

**Output:**

```php
This is non-static
This is static

```

然而，静态方法不允许您定义显式依赖关系，并且在代码中包含可以从任何地方访问的全局变量。这会影响应用程序的可伸缩性。此外，您将很难对包含静态方法的类执行自动化测试。因此，它们应该用于公用事业，而不是为了方便。

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。