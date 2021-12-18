# PHPUnit assertIsBool()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisbool-function/](https://www.geeksforgeeks.org/phpunit-assertisbool-function/)

**assertIsBool()**函数是 PHPUnit 中的内置函数，用于断言实际获得的值是否为 Bool。 如果实际值为布尔值，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertIsBool($actual[, $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$ActualValue:** this parameter can be any type that represents the actual data.
*   **$Message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的 assertIsBool()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeForassertIsNotBooltrue()
    {    $actual = 420;
        // Assert function to test whether actual 
        // value is (true or false) or not
        $this->assertIsBool( 

            $actual, 
            "actual value is Bool or not"
        );

    }

    public function testNegativeForassertIsNotBoolFalse()
    {  
        $actual = 220;
        // Assert function to test whether actual
        // value is (true or false) or not

        $this->assertIsBool( 

            $actual, 
            "actual value is Bool or not"
        );
    }  
 } 
?> 
```

发帖主题：Re：Колибри0.7.8.0

示例 2：

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveForassertIsNotBooltrue()
    {    $actual = true;
        // Assert function to test whether actual 
        // value is (true or false) or not
        $this->assertIsBool( 

            $actual, 
            "actual value is Bool or not"
        );

    }

    public function testPositiveForassertIsNotBoolFalse()
    {  
        $actual = false;
        // Assert function to test whether actual
        // value is (true or false) or not

        $this->assertIsBool( 

            $actual, 
            "actual value is Bool or not"
        );
    }  
 } 
?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertisbool](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertisbool)