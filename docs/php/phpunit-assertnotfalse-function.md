# PHPUnit assertNotFalse()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertnotfalse-function/](https://www.geeksforgeeks.org/phpunit-assertnotfalse-function/)

**assertNotFalse()**函数是 PHPUnit 中的内置函数，用于断言条件值为真。 如果条件值为 TRUE，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertNotFalse(bool $condition[, string $message = ''])

```

**参数：**此函数接受上述三个参数，如下所述：

*   **$Condition：**此参数可以是表示 TRUE 或 FALSE 的任何类型的值。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertNotfalse()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertNotFalse()
    { 
        $condition = false;

        // Assert function to test whether
        // condition value is true or not 
        $this->assertNotFalse(

            $condition, 
            "condition is true or false"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                  1 / 1 (100%)

Time: 95 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeTestcaseForassertNotFalse
condition is true or false
Failed asserting that false is not false.

/home/lovely/Documents/php/test.php:17

FAILURES!
Tests: 1, Assertions: 1, Failures: 1.

```

**示例 2：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPsitiveTestcaseForassertNotFalse()
    { 
        $condition = "false";

        // Assert function to test whether
        // condition value is true or not 
        $this->assertNotFalse(

            $condition, 
            "condition is true or false"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                 1 / 1 (100%)

Time: 91 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)

```