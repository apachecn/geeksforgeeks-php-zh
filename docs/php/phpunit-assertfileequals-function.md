# PHPUnit assertFileEquals()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertfileequals-function/](https://www.geeksforgeeks.org/phpunit-assertfileequals-function/)

**assertFileEquals()**函数是 PHPUnit 中的内置函数，用于断言实际文件内容是否与预期文件内容完全相同。 如果预期文件内容与实际文件内容相同，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertFileEquals(string $expected, 
      string $actual[, string $message = ''])

```

**参数：**此函数接受三个参数，如上所述，如下所述：

*   **$Expect:** this parameter is a string that represents the expected file path.
*   **$Actual:** this parameter is a string that represents the actual file path.
*   **$message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下程序说明了 PHPUnit 中的 assertFileEquals()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertFileEquals() 
    { 
        $expected = "/home/bittu/php"; 
        $actual = "/home/bittu/Documents"; 

        // Assert function to test whether expected 
        // file content is equal to actual file content or not 
        $this->assertFileEquals(
            $expected, 
            $actual, 
"actual file content is not equals to expected file content"
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
    public function testPositiveTestcaseForassertFileEquals() 
    { 
        $expected = "/home/bittu/Documents"; 
        $actual = "/home/bittu/Documents"; 

        // Assert file equal function to test whether expected 
        // file content is equal to actual file content or not 
        $this->assertFileEquals(
            $expected, 
            $actual, 
"actual file content is not equals to expected file content"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertfileequals](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertfileequals)