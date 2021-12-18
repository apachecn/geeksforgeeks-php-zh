# PHPUnit assertIsNotArray()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisnotarray-function/](https://www.geeksforgeeks.org/phpunit-assertisnotarray-function/)

**assertIsNotArray()**函数是 PHPUnit 中的内置函数，用于断言给定变量是否不是数组。 如果给定变量不是数组，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertIsNotArray($actual[, $message = ''])
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Variable：**此参数可以是表示实际数据的任何类型的变量。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertIsNotArray()函数：

**示例 1：**

## PHP

```php
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testNegativeForassertIsNotArray()

    { 
     $variable  = array ("apple/banana");
         // Assert function to test whether assert
        //  variable is array
        $this->assertIsNotArray(
            $variable,
            "assert variable is array"
        );

    }

 }
?>
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                 1 / 1 (100%)

Time: 87 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeForassertIsNotArray
assert variable is array or not
Failed asserting that Array &0 (
  0 => 'apple/banana'
) is not of type "array".

/home/lovely/Documents/php/test.php:15

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
    public function testPositiveForassertIsNotArray()

    { 
     $variable  = ("apple/banana");
         // Assert function to test whether assert
        //  variable is array or not
        $this->assertIsNotArray(
            $variable,
            "assert variable is array"
        );

    }

 }
?>
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                 1 / 1 (100%)

Time: 87 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)
```