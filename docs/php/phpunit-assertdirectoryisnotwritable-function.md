# PHPUnit assertDirectoryIsNotWritable()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertdirectoryisnotwritable-function/](https://www.geeksforgeeks.org/phpunit-assertdirectoryisnotwritable-function/)

**assertDirectoryIsNotWritable()**函数是 PHPUnit 中的内置函数，用于断言指定的目录是否为不可写目录。 如果给定的目录路径不存在或不可写，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertDirectoryIsNotWritable(string $directory[, string $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$directory:** this parameter is a string that represents the directory path.
*   **$Message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下程序说明了 PHPUnit 中的 assertDirectoryIsNotWritable()函数：

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
        // directory path exists and writable or not
        $this->assertDirectoryIsWritable( 
            $directoryPath, 
            "directory Path exists and is writable"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.8.0

示例 2：

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

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/8.2/assertions.html#assertdirectoryi](https://phpunit.readthedocs.io/en/8.2/assertions.html#assertdirectoryi)