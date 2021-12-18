# PHPUnit assertFileExists()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertfileexists-function/](https://www.geeksforgeeks.org/phpunit-assertfileexists-function/)

**assertFileExists()**函数是 PHPUnit 中的内置函数，用于检查文件路径是否存在。 如果给定的文件路径存在，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertFileExists(string $filename[, string $message = ''])
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$filename:** this parameter is a string that represents the file path.
*   **$Message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下程序说明了 PHPUnit 中的 assertFileExists()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForAssertFileExists() 
    { 
        $filename = "/home/Documents/geeksDoesNotExist/"; 

        // Assert function to test whether given 
        // file path exists or not 
        $this->assertFileExists( 
            $filename, 
            "given filename doesn't exists"
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
    public function testPositiveTestcaseForAssertFileExists() 
    { 
        $filename = "/home/bittu/Documents/php/"; 

        // Assert function to test whether given 
        // file name exists or not 
        $this->assertFileExists( 
            $filename, 
            "filename doesn't exists"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/8.2/assertions.html#assertfileexists](https://phpunit.readthedocs.io/en/8.2/assertions.html#assertfileexists)