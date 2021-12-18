# PHPUnit assertNotIsWritable()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertnotiswritable-function/](https://www.geeksforgeeks.org/phpunit-assertnotiswritable-function/)

**assertNotIsWritable()**函数是 PHPUnit 中的内置函数，用于断言 assertNotIsWritable 是否指定该文件名不可写。 如果给定的文件名不存在且不可写，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertNotIsWritable(string $filename[, string $message = ''])

```

**参数：**此函数接受两个参数，如上面的语法所示。 具体参数说明如下：

*   **$filename：**此参数是表示文件名的任何类型的字符串。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertNotIsWritable()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertNotIsWritable()
    { 
        $filename = "/home/lovely/Documents/php/phpunit"; 

        // Assert function to test whether given 
        // file name is not writable 
        $this->assertNotIsWritable(
            $filename, 
            "filename is not writable"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                             1 / 1 (100%)

Time: 85 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeTestcaseForassertNotIsWritable
filename is writable or Not
Failed asserting that "/home/lovely/Documents/php/phpunit" is not writable.

/home/lovely/Documents/php/test.php:16

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
    public function testPositiveTestcaseForassertNotIsWritable()
    { 
        $filename = "/home/lovely/Documents/php/phpunit/geeksforgeeks"; 

        // Assert function to test whether given 
        // file name is not writable 
        $this->assertNotIsWritable(
            $filename, 
            "filename is writable or not"
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