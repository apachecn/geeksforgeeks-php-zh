# PHPUnit assertDirectoryIsWritable()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertdirectoryiswritable-function/](https://www.geeksforgeeks.org/phpunit-assertdirectoryiswritable-function/)

**assertDirectoryIsWritable()**函数是 PHPUnit 中的内置函数，用于断言指定的目录是目录还是可写目录。 如果给定的目录路径存在且可写，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertDirectoryIsWritable(string $directory[, string $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$directory：**此参数是表示目录路径的字符串。
*   **$message：**此参数接受字符串值。 当测试用例失败时，该字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertDirectoryIsWritable()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForAssertDirectoryIsWritable() 
    { 
        $directoryPath = "/home/lovely/Documents/writable"; 

        // Assert function to test whether given 
        // directory path exists and writable
        $this->assertDirectoryIsWritable( 
            $directoryPath, 
            "directoryPath exists and writable"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                         1 / 1 (100%)

Time: 90 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeTestcaseForAssertDirectoryIsWritable
directoryPath exists and writable
Failed asserting that directory "/home/lovely/Documents/writable" exists.

/home/lovely/Documents/php/test.php:15

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
    public function testPositiveTestcaseForAssertDirectoryIsWritable() 
    { 
        $directoryPath = "/home/lovely/Documents"; 

        // Assert function to test whether given 
        // directory path exists and writable
        $this->assertDirectoryIsWritable( 
            $directoryPath, 
            "directoryPath exists and writable"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                             1 / 1 (100%)

Time: 89 ms, Memory: 10.00 MB

OK (1 test, 2 assertions)

```