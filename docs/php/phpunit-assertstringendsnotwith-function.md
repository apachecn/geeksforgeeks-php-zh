# PHPUnit assertStringEndsNotWith()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertstringendsnotwith-function/](https://www.geeksforgeeks.org/phpunit-assertstringendsnotwith-function/)

**assertStringEndsNotWith()**函数是**PHPUnit**中的内置函数，用于断言实际字符串是否没有以预期的后缀字符串结尾。 如果实际字符串没有以预期的后缀字符串结尾，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertStringEndsNotWith(string $suffix, string $string
[, string $message = ''])

```

**参数：**此函数接受上述三个参数，如下所述：

*   **$expectedSuffix：**此参数可以是表示预期后缀字符串的任何类型。
*   **$ActualString：**此参数可以是表示实际字符串的任何类型。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertStringEndsNotWith()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertStringEndsNotWith()
    { 
        $expectedsuffix = ('th');
        $actualstring = ('4th');

        // Assert function to test whether expected suffix
        // string doesn't ends with actual string content
        $this->assertStringEndsNotWith(
            $expectedsuffix,
            $actualstring, 
            "actual string content doesn't ends with 
             expected suffix content"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                          1 / 1 (100%)

Time: 88 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeTestcaseForassertStringEndsNotWith
actual string content doesn't ends with expected suffix content
Failed asserting that '4th' ends not with "th".

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
    public function testPositiveTestcaseForassertStringEndsNotWith()
    { 
        $expectedsuffix = ('rd');
        $actualstring = ('4th');

        // Assert function to test whether expected suffix
        // string doesn't ends with actual string content
        $this->assertStringEndsNotWith(
            $expectedsuffix,
            $actualstring, 
            "actual string content doesn't ends with 
             expected suffix content"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                  1 / 1 (100%)

Time: 87 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)

```