# PHPUnit assertIsObject()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisobject-function/](https://www.geeksforgeeks.org/phpunit-assertisobject-function/)

**assertIsObject()**函数是 PHPUnit 中的内置函数，用于断言实际给定的内容是否为对象。 如果实际给定的内容是 Object，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 True，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertIsObject($actual[, $message = ''])

```

**参数：**此函数接受两个参数，如下所述：

*   **$Actual:** this parameter can be any type that represents the actual content.
*   **$Message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

下面的示例说明了 PHPUnit 中的**assertIsObject()**函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertIsObject() 
    { 
        $actualcontent =  ('lovely laptop');

        // Assert function to test whether given 
        // actual content is object or not
        $this->assertIsObject(
            $actualcontent, 
            "actual content is object or not"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.8.0

示例 2：

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveTestcaseForassertIsObject() 
    { 
        $actualcontent = (object) ('lovely laptop');

        // Assert function to test whether given 
        // actual content is object or not
        $this->assertIsObject(
            $actualcontent, 
            "actual content is object or not"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertisobject](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertisobject)