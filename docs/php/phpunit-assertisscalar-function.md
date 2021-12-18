# PHPUnit assertIsScalar()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisscalar-function/](https://www.geeksforgeeks.org/phpunit-assertisscalar-function/)

**assertIsScalar()**函数是 PHPUnit 中的内置函数，用于断言标量变量是包含整数、浮点数、字符串或布尔值的变量。 此函数不将 NULL 视为标量。 如果实际值是标量，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertIsScalar($actual[, $message = ''])

```

**参数：**此函数接受下面提到和描述的两个参数：

*   **$Actual:** this parameter can be any type of string or variable that represents the actual data.
*   **$Message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的 assertIsScalar()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeForassertIsScalar()
    {   
     $actualvalue = Null;
        // Assert function to test whether actual 
        // value is a scalar or not
        $this->assertIsScalar(

            $actualvalue, 
            "actual value is a scalar or not"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveForassertIsScalar()
    {   
     $actualvalue = "Null";
        // Assert function to test whether actual 
        // value is a any type of string or not
        $this->assertIsScalar(

            $actualvalue, 
            "actual value is a scalar or not"
        );

    }

     public function testNegativeForassertIsScalar()
    {   
     $actualvalue = 420;
            // Assert function to test whether actual 
        // value is a integer or not
        $this->assertIsScalar(

            $actualvalue, 
            "actual value is a scalar or not"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertisscalar](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertisscalar)