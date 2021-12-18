# PHPUnit assertNotSame()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertnotsame-function/](https://www.geeksforgeeks.org/phpunit-assertnotsame-function/)

**assertNotSame()**函数是**PHPUnit**中的内置函数，用于断言实际获得的值与期望值不同。 如果期望值与实际值不同，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertNotSame( mixed $expected, mixed $actual, string $message = '' )

```

**参数：**此函数接受三个参数，如上面的语法所示。 具体参数说明如下：

*   **$Expect：**此参数可以是表示预期数据的任何类型。
*   **$Actual：**此参数可以是表示实际数据的任何类型。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertNotSame()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeForassertNotSame()

    {
     $expected = "(108) mango";    
     $actual = "(108) mango";
        // Assert function to test whether expected
        // value is same as actual value or not
        $this->assertNotSame(
            $expected,
            $actual,
            "actual value is same to expected"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                 1 / 1 (100%)

Time: 90 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeForassertNotSame
actual value is same to expected
Failed asserting that two strings are not identical.

/home/lovely/Documents/php/test.php:17

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
    public function testPositiveForassertNotSame()

    {
     $expected = "(108) banana";    
     $actual = "(108) mango";
        // Assert function to test whether expected
        // value is same as actual value or not
        $this->assertNotSame(
            $expected,
            $actual,
            "actual value is same to expected"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                  1 / 1 (100%)

Time: 90 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)

```