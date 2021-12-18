# PHPUnit assertIsFloat()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisfloat-function/](https://www.geeksforgeeks.org/phpunit-assertisfloat-function/)

**assertIsFloat()**函数是 PHPUnit 中的内置函数，用于断言实际获得的值是否为浮点值。 如果实际值为 Float，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertIsFloat($actual[, $message = ''])
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Actual:** this parameter can be any type of integer that represents the actual data.
*   **$Message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的 assertIsFloat()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeForassertIsFloat()
    {    $actualvalue = (420);
        // Assert function to test whether actual 
        // value is float or not
        $this->assertIsFloat(

            $actualvalue, 
            "actual value is float or not"
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
    public function testPositiveForassertIsFloat()
    {    $actualvalue = (4.20);
        // Assert function to test whether actual 
        // value is float or not
        $this->assertIsFloat(

            $actualvalue, 
            "actual value is float or not"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertisfloat](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertisfloat)