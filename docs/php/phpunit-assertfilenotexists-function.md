# PHPUnit assertFileNotExists()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertfilenotexists-function/](https://www.geeksforgeeks.org/phpunit-assertfilenotexists-function/)

**assertFileNotExists()**函数是 PHPUnit 中的内置函数，用于断言文件是否存在于给定路径。 如果给定的文件路径不存在，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertFileNotExists(string $filename[, string $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$filename：**此参数是表示文件路径的字符串。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下程序说明了 PHPUnit 中的 assertFileNotExists()函数：

**程序 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForAssertFileNotExists() 
    { 
        $filename = "/home/bittu/Documents/php/"; 

        // Assert function to test whether given 
        // file name exists or not 
        $this->assertFileNotExists( 
            $filename, 
            "filename exists at given path"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                             1 / 1 (100%)

Time: 391 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeTestcaseForAssertFileNotExists
filename exists at given path
Failed asserting that file "/home/bittu/Documents/php/" not exists.

/home/lovely/Documents/php/test.php:15

FAILURES!
Tests: 1, Assertions: 1, Failures: 1.
```

节目 2：

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveTestcaseForAssertFileNotExists() 
    { 
        $filename = "/home/Documents/geeksDoesNotExist/"; 

        // Assert function to test whether given 
        // file name exists or not 
        $this->assertFileNotExists( 
            $filename, 
            "filename exists"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                             1 / 1 (100%)

Time: 88 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)
```