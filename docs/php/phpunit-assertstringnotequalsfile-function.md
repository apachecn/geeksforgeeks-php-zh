# PHPUnit assertStringNotEqualsFile()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertstringnotequalsfile-function/](https://www.geeksforgeeks.org/phpunit-assertstringnotequalsfile-function/)

**assertStringNotEqualsFile()**函数是**PHPUnit**中的内置函数，用于断言实际字符串内容是否与预期文件不同。 如果预期的文件内容与实际字符串内容不同，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertStringNotEqualsFile(string $expectedFile, 
string $actualString[, string $message = ''])

```

**参数：**此函数接受上述三个参数，如下所述：

*   **$expectedfile：**此参数可以是表示预期文件的任何类型。
*   **$ActualString：**此参数可以是表示实际字符串内容的任何类型。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertStringNotEqualsFile()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertStringNotEqualsFile()
    { 
        $expectedfile = "/home/lovely/Documents/php/abc";
        $actualstring = "File has not geeksforgeeks"; 

        // Assert function to test whether expected file 
        // content is equal to actual string content
        $this->assertStringNotEqualsFile(
            $expectedfile,
            $actualstring, 
            "actual string content is equals to
             expected file content"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                  1 / 1 (100%)

Time: 86 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testPositiveTestcaseForassertStringNotEqualsFile
actual string content is equals to expected file content
Failed asserting that 'File does not have not geeksforgeeks' 
is not equal to 'File does not have not geeksforgeeks'.

/home/lovely/Documents/php/test.php:17

FAILURES!
Tests: 1, Assertions: 2, Failures: 1.

```

**示例 2：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveTestcaseForassertStringNotEqualsFile()
    { 
        $expectedfile = "/home/lovely/Documents/php/abc";
        $actualstring = "File has geeksforgeeks"; 

        // Assert function to test whether expected file 
        // content is equal to actual string content
        $this->assertStringNotEqualsFile(
            $expectedfile,
            $actualstring, 
            "actual string content is equals to 
             expected file content"
        ); 
    } 
}
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                  1 / 1 (100%)

Time: 88 ms, Memory: 10.00 MB

OK (1 test, 2 assertions)

```