# PHPUnit|assertNotContainsOnly()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertnotcontainsonly-function/](https://www.geeksforgeeks.org/phpunit-assertnotcontainsonly-function/)

**assertNotContainsOnly()**函数是 PHPUnit 中的一个内置函数，用于断言一个数组不包含作为给定数据类型的所有值。 如果数组包含给定数据类型以外的值，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertNotContainsOnly( string $dataType, array $array,
                 boolean $isNativeType = null, string $message = '' )

```

**参数：**此函数接受四个参数，如上面的语法所示。 参数说明如下：

*   **$dataType:** this parameter is a string consisting of the data type name.
*   **$ARRAY:** this parameter is an array, and the Assert function will check whether it contains only values of the given type.
*   **$isNativeType:** this parameter indicates whether the data type is a PHP native data type.
*   **$message:** this parameter accepts string values. When the test case fails, the string message is displayed as an error message.

以下程序说明了 PHPUnit 中的 assertNotContainsOnly()函数：

**程序 1：**

```
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testNegativeTestcaseForAssertNotContainsOnly()
    {
        $testArray = array("geeksforgeek", "true");
        $dataType = "string"; 

        // Assert function to test whether testArray contains
        // only string values or not
        $this->assertNotContainsOnly($dataType, $testArray, null,
                 "testArray contains only string") ;
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testPositiveTestcaseForAssertNotContainsOnly()
    {
        $testArray = array("geeksforgeek", 4);
        $dataType = "string"; 

        // Assert function to test whether testArray contains
        // only string values
        $this->assertNotContainsOnly($dataType, $testArray, null,
               "testArray  contains only string") ;
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**要使用 phpunit 运行测试用例，请执行此处[中的步骤](https://www.jetbrains.com/help/phpstorm/using-phpunit-framework.html)。 此外，phpunit 7 及更高版本支持 assertNotContainsOnly()。