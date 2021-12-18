# PHPUnit assertIsWritable()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertiswritable-function/](https://www.geeksforgeeks.org/phpunit-assertiswritable-function/)

函数的作用是：**assertIsWritable()**是 PHPUnit 中的一个内置函数，用于断言 assertisWritable 是否指定了该文件名是可写的。 如果给定的文件名存在且可写，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertIsWritable(string $filename[, string $message = ''])

```

**参数：**此函数接受两个参数，如上面的语法所示。 参数描述如下：

*   **$filename:** this parameter is any type of string that represents the file name.
*   **$Message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的 assertIsWritable()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertIsWritable()
    { 
        $filename = "/home/lovely/Documents/php/GeeksPhpunitTestCase"; 

        // Assert function to test whether given 
        // file name is writable or not 
        $this->assertIsWritable(
            $filename, 
            "filename is writable or Not"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveTestcaseForassertIsWritable()
    { 
        $filename = "/home/lovely/Documents/php"; 

        // Assert function to test whether given 
        // file name is writable or not 
        $this->assertIsWritable(
            $filename, 
            "filename is writable or Not"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertiswritable](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertiswritable)