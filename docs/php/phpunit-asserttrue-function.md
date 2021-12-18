# PHPUnit assertTrue()函数

> Original: [https://www.geeksforgeeks.org/phpunit-asserttrue-function/](https://www.geeksforgeeks.org/phpunit-asserttrue-function/)

**assertTrue()**函数是 PHPUnit 中的内置函数，用于断言断言值是否为真。 如果断言值为 TRUE，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertTrue(bool $condition[, string $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$assertvalue:** this parameter can be any type of variable that represents assertion data.
*   **$Message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的 assertTrue()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeForassertTrue()

    {  
     $assertvalue = false;
        // Assert function to test whether assert
        // value is true or not
        $this->assertTrue(
            $assertvalue,
            "assert value is true or not"
        );

    }

 } 
?> 
S
```

发帖主题：Re：Колибри0.7.8.0

示例 2：

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveForassertTrue()

    {  
     $assertvalue = true;
        // Assert function to test whether assert
        // value is true or not
        $this->assertTrue(
            $assertvalue,
            "assert value is true or not"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#asserttrue](https://phpunit.readthedocs.io/en/9.2/assertions.html#asserttrue)