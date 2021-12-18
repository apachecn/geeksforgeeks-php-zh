# PHPUnit assertSame()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertsame-function/](https://www.geeksforgeeks.org/phpunit-assertsame-function/)

**assertSame()**函数是 PHPUnit 中的内置函数，用于断言实际获得的值是否与期望值相同。 如果期望值与实际值相同，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertSame(mixed $expected, mixed $actual[, string $message = ''])

```

**参数：**此函数接受三个参数，如上所述，如下所述：

*   **$Expect:** this parameter can be any type that represents the expected data.
*   **$Actual:** this parameter can be any type that represents the actual data.
*   **$message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的 assertSame()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeForassertSame()

    {
     $expected = "(108) banana";    
     $actual = "(108) mango";
        // Assert function to test whether expected
        // value is same as actual value or not
        $this->assertSame(
            $expected,
            $actual,
            "actual value is not same as expected value"
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
    public function testPositiveForassertSame()

    {
     $expected = "(108) mango";    
     $actual = "(108) mango";
        // Assert function to test whether expected
        // value is same as actual value or not
        $this->assertSame(
            $expected,
            $actual,
            "actual value is not same as expected value"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertsame](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertsame)