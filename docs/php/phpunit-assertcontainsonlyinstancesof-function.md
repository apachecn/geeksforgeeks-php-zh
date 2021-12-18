# PHPunit|assertContainsOnlyInstancesOf()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertcontainsonlyinstancesof-function/](https://www.geeksforgeeks.org/phpunit-assertcontainsonlyinstancesof-function/)

**assertContainsOnlyInstancesOf()**函数是 PHPUnit 中的一个内置函数，用于断言一个数组将其所有值作为给定类的实例。 如果数组只包含给定类的实例，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertContainsOnlyInstancesOf( string $classname, array $array, string $message = '' )

```

**参数：**此函数接受三个参数，如上面的语法所示。 参数描述如下：

*   **$className:** this parameter is a string, which is the name of the class.
*   **$ARRAY:** this parameter is an array, and the Assert function checks whether it contains only instances of the given class.
*   **$message:** this parameter accepts string values. When the test case fails, the string message is displayed as an error message.

以下程序说明了 PHPUnit 中的 assertContainsOnlyInstancesOf()函数：

**程序 1：**

```
<?php

use PHPUnit\Framework\TestCase;

class Foo {
    public function dummyFunction(){return true;}
}

class Bar {
    public function dummyFunction(){return true;}
}

class GeeksPhpunitTestCase extends TestCase
{
    public function testNegativeTestcaseForAssertContainsOnlyInstancesOf()
    {

        // Assert function to test whether testArray contains
        // only instance of Foo or not
        $this->assertContainsOnlyInstancesOf(
            Foo::class,
            [new Foo, new Bar, new Foo], 
            "testArray doesn't contains only instance of Foo"
        );
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php
use PHPUnit\Framework\TestCase;

class Foo {
    public function dummyFunction(){return true;}
}

class Bar {
    public function dummyFunction(){return true;}
}

class GeeksPhpunitTestCase extends TestCase
{
    public function testNegativeTestcaseForAssertContainsOnlyInstancesOf()
    {
        // Assert function to test whether testArray contains
        // only instance of Foo or not
        $this->assertContainsOnlyInstancesOf(
            Foo::class,
            [new Foo, new Foo],
            "testArray contains only instance of Foo"
        );
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**要使用 phpunit 运行测试用例，请执行此处[中的步骤](https://www.jetbrains.com/help/phpstorm/using-phpunit-framework.html)。 此外，phpunit 7 及更高版本支持 assertContainsOnlyInstancesOf()。