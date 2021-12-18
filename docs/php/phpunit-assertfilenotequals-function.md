# PHPUnit assertFileNotEquals()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertfilenotequals-function/](https://www.geeksforgeeks.org/phpunit-assertfilenotequals-function/)

**assertFileNotEquals()**函数是 PHPUnit 中的内置函数，用于断言实际文件内容是否与预期文件内容不同。 如果预期文件内容不等于实际文件内容，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertFileNotEquals(string $expected, string $actual[, string $message = ''])
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$Expect：**此参数为字符串类型，表示预期的文件路径。
*   **$Actual：**此参数为字符串类型，表示实际文件路径。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下程序说明了 PHPUnit 中的 assertFileNotEquals()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertFileNotEquals() 
    { 
        $expected = "/home/bittu/Documents"; 
        $actual = "/home/bittu/Documents"; 

        // Assert file not equal function to test whether expected 
        // file content is different to actual file content or not 
        $this->assertFileNotEquals(
            $expected, 
            $actual, 
            "actual file content is equals to expected file content"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                             1 / 1 (100%)

Time: 116 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeTestcaseForassertFileNotEquals
actual file content is equals to expected file content
Failed asserting that file "/home/bittu/Documents" exists.

/home/lovely/Documents/php/test.php:17

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
    public function testPositiveTestcaseForassertFileNotEquals() 
    { 
        $expected = "/home/bittu/Documents/php/demo.txt"; 
        $actual = "/home/bittu/Documents/php/file1.php"; 

        // Assert file not equal function to test whether expected 
        // file content is different from actual file content or not 
        $this->assertFileNotEquals(
            $expected, 
            $actual, 
            "actual file content is equals to expected file content"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                             1 / 1 (100%)

Time: 91 ms, Memory: 10.00 MB

OK (1 test, 3 assertions)
```