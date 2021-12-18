# PHPUnit assertNotEqualsIgnoringCase()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertnotequalsignoringcase-function/](https://www.geeksforgeeks.org/phpunit-assertnotequalsignoringcase-function/)

AssertNotEqualsIgnoringCase()函数是 PHPUnit 中的内置函数，用于断言预期字符串是否不等于实际字符串，但忽略大小写。 如果实际字符串不等于预期字符串(忽略区分大小写)，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertnotEqualsIgnoringCase(mixed $expected, 
        mixed $actual[, string $message = '']

```

**参数：**此函数接受上述三个参数，如下所述：

*   **$Expect：**此参数是表示预期数据的字符串。
*   **$Actual：**此参数是表示实际数据的字符串。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下程序说明了 assertnotEqualsIgnoringCase()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativTestcaseForAssertNotequalIgnoringCase() 
    { 
        $expected = "Geeks"; 
        $actual= "geEks";  
        // assert function to test whether expected
        // is not equals to actual ignoring case
        $this->assertNotEqualsIgnoringCase(
            $actual, 
            $expected,
        "expected string is equal to actual ignoring case" ) ; 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                             1 / 1 (100%)

Time: 91 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testpositivTestcaseForAssertNotequalIgnoringCase
expected string is equal to actual ignoring case
Failed asserting that 'Geeks' is not equal to 'geEks'.

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
    public function testPositivTestcaseForAssertNotequalIgnoringCase() 
    { 
        $expected = "Geekss"; 
        $actual= "geEks";  
        // assert function to test whether expected
        // is not equals to actual string ignoring case
        $this->assertNotEqualsIgnoringCase(
            $actual, 
            $expected,
        "expected string is equal to actual ignoring case" ) ; 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                             1 / 1 (100%)

Time: 91 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)

```