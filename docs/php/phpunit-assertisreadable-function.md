# PHPUnit assertIsReadable()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisreadable-function/](https://www.geeksforgeeks.org/phpunit-assertisreadable-function/)

**assertIsReadable()**函数是 PHPUnit 中的内置函数，用于断言 assertIsReadable 指定的文件名是否可读。 如果给定的文件名是可读的，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertIsReadable(string $filename[, string $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$filename:** this parameter is a string representing the file name.
*   **$Message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的 assertIsReadable()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertIsReadable()
    { 
        $filename = "/home/lovely/Documents/phptest"; 

        // Assert function to test whether given 
        // file name is readablee or not 
        $this->assertIsReadable(
            $filename, 
            "filename is readable or Not"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.8.0

示例 2：

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveTestcaseForassertIsReadable()
    { 
        $filename = "/home/lovely/Documents"; 

        // Assert function to test whether given 
        // file name is readablee or not 
        $this->assertIsReadable(
            $filename, 
            "filename is readable or Not"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertisreadable](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertisreadable)