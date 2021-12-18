# PHPUnit assertStringEqualsFile()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertstringequalsfile-function/](https://www.geeksforgeeks.org/phpunit-assertstringequalsfile-function/)

**assertStringEqualsFile()**函数是**PHPUnit**中的内置函数，用于断言获得的实际字符串内容是否等于预期的文件。 如果预期的文件内容与实际字符串内容相同，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertStringEqualsFile(string $expectedFile, 
string $actualString[, string $message = ''])

```

**参数：**此函数接受上述三个参数，如下所述：

*   **$expectedfile:** this parameter can be any type that represents the expected file.
*   **$ActualString:** this parameter can be any type that represents the contents of the actual string.
*   **$message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的 assertStringEqualsFile()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertStringEqualsFile()
    { 
        $expectedfile = "/home/lovely/Documents/php/abc";
        $actualstring = "File has geeksforgeeks"; 

        // Assert function to test whether 
        // expected file content is equal to 
        // actual string content or not 
        $this->assertStringEqualsFile(
            $expectedfile,
            $actualstring, 
            "actual string content is equals to
             expected file content or not"
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
    public function testPositiveTestcaseForassertStringEqualsFile()
    { 
        $expectedfile = "/home/lovely/Documents/php/abc";
        $actualstring = "File has geeksforgeeks"; 

        // Assert function to test whether 
        // expected file content is equal 
        // to actual string content or not 
        $this->assertStringEqualsFile(
            $expectedfile,
            $actualstring, 
            "actual string content is equals 
             to expected file content or not"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertstringequalsfile](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertstringequalsfile)