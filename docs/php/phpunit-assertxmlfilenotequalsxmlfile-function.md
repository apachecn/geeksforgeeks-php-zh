# PHPUnit assertXmlFileNotEqualsXmlFile()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertxmlfilenotequalsxmlfile-function/](https://www.geeksforgeeks.org/phpunit-assertxmlfilenotequalsxmlfile-function/)

**assertXmlFileNotEqualsXmlFile()**函数是 PHPUnit 中的内置函数，用于断言实际的 XML 文件内容是否不等于预期的 XML 文件内容。 如果预期的 XML 文件内容与实际的 XML 文件内容不同，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertXmlFileNotEqualsXmlFile(string $expectedFile, 
string $actualFile[, string $message = ''])

```

**参数：**此函数接受上述三个参数，如下所述：

*   **$expectedFile：**此参数可以是表示预期 XML 文件路径的任何类型。
*   **$ActualFile：**此参数可以是表示实际 XML 文件路径的任何类型。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertXmlFileNotEqualsXmlFile()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertXmlFileNotEqualsXmlFile()
    { 
        $actualFile =  '/home/lovely/Documents/php/actual.xml';
        $expectedFile    = '/home/lovely/Documents/php/expected.xml'; 
        // Assert function to test whether given 
        // expected xml file is not equal to actual xml file
        $this->assertXmlFileNotEqualsXmlFile(
            $actualFile,
            $expectedFile, 
            "actual xml file is not equal to expected xml file"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                               1 / 1 (100%)

Time: 89 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeTestcaseForassertXmlFileNotEqualsXmlFile
actual xml file is not equal to expected xml file
Failed asserting that DOMDocument Object &000000000788a1260000000067204f26 
() is not equal to DOMDocument Object &000000000788a1210000000067204f26 ().

/home/lovely/Documents/php/test.php:16

FAILURES!
Tests: 1, Assertions: 1, Failures: 1.

```

**示例 2：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveTestcaseForassertXmlFileNotEqualsXmlFile()
    { 
        $actualFile =  '/home/lovely/Documents/php/actual.xml';
        $expectedFile    = '/home/lovely/Documents/php/expected.xml'; 
        // Assert function to test whether given 
        // expected xml file is not equal to actual xml file
        $this->assertXmlFileNotEqualsXmlFile(
            $actualFile,
            $expectedFile, 
            "actual xml file is not equal to expected xml file"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                1 / 1 (100%)

Time: 88 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)

```