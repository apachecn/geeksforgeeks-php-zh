# PHPUnit assertNotIsReadable()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertnotisreadable-function/](https://www.geeksforgeeks.org/phpunit-assertnotisreadable-function/)

**assertNotIsReadable()**函数是 PHPUnit 中的内置函数，用于断言 assertNotIsReadable 指定的文件名是否不可读。 如果给定的文件名不可读，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertNotIsReadable(string $filename[, string $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$filename：**此参数是表示文件名的字符串。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertNotIsReadable()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertNotIsReadable()
    { 
        $filename = "/home/lovely/Documents"; 

        // Assert function to test whether given 
        // file name is readablee or not 
        $this->assertNotIsReadable(
            $filename, 
            "filename is readable or Not"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                     1 / 1 (100%)

Time: 88 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeTestcaseForassertNotIsReadable
filename is readable or Not
Failed asserting that "/home/lovely/Documents" is not readable.

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
    public function testPositiveTestcaseForassertNotIsReadable()
    { 
        $filename = "/home/lovely/Documents/phptest"; 

        // Assert function to test whether given 
        // file name is readablee or not 
        $this->assertNotIsReadable(
            $filename, 
            "filename is readable or Not"
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