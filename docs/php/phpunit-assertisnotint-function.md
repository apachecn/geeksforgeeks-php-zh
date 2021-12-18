# PHPUnit assertIsNotInt()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisnotint-function/](https://www.geeksforgeeks.org/phpunit-assertisnotint-function/)

**assertIsNotInt()**函数是 PHPUnit 中的内置函数，用于断言给定的实际变量是否不是整数。 如果实际变量不是整数，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertIsNotInt($actual[, $message = ''])
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Actual：**此参数可以是表示实际数据的任何类型的变量。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertIsNotInt()函数：

**示例 1：**

## PHP

```
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testNegativeForassertIsNotInt()

    {  
     $actualvalue = 101;
        // Assert function to test whether actual
        // variable is doesn't Integer
        $this->assertIsNotInt(

            $actualvalue,
            "actual value is Doesn't Integer"
        );

    }

 }
?>
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                  1 / 1 (100%)

Time: 89 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeForassertIsNotInt
actual value is Doesn't Integer
Failed asserting that 101 is not of type "int".

/home/lovely/Documents/php/test.php:16

FAILURES!
Tests: 1, Assertions: 1, Failures: 1.
```

**示例 2：**

## PHP

```
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testPositiveForassertIsNotInt()

    {  
     $actualvalue = 101.99;
        // Assert function to test whether actual
        // variable is doesn't Integer
        $this->assertIsNotInt(

            $actualvalue,
            "actual value is Doesn't Integer"
        );

    }

 }
?>
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                  1 / 1 (100%)

Time: 95 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)
```