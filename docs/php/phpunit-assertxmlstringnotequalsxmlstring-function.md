# PHPUnit assertXmlStringNotEqualsXmlString()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertxmlstringnotequalsxmlstring-function/](https://www.geeksforgeeks.org/phpunit-assertxmlstringnotequalsxmlstring-function/)

**assertXmlStringNotEqualsXmlString()**函数是 PHPUnit 中的内置函数，用于断言实际的 XML 字符串是否不等于预期的 XML 字符串。 如果期望的 XML 字符串与实际的 XML 字符串不同，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertXmlStringNotEqualsXmlString(string $expectedXml, 
string $actualXml[, string $message = ''])

```

**参数：**此函数接受上述三个参数，如下所述：

*   **$expectedXmlString：**此参数可以是表示预期 XML 字符串的任何类型。
*   **$ActualXmlString：**此参数可以是表示实际 XML 字符串的任何类型。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

下面的示例说明了 PHPUnit 中的 assertXmlStringNotEqualsXmlString()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertXmlStringNotEqualsXmlString()
    { 
        $expectedxmlString  =  '<foo><baz></baz></foo>'; 
        $actualxmlString    =  '<foo><baz></baz></foo>';
        // Assert function to test whether given 
        // expected xml string is not equal to actual xml string
        $this->assertXmlStringNotEqualsXmlString(
            $actualxmlString,
            $expectedxmlString,
            "actual xml string is not equal to expected xml string"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                                1 / 1 (100%)

Time: 89 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testPositiveTestcaseForassertXmlFileNotEqualsXmlFile
actual xml string is equal to expected xml string
Failed asserting that DOMDocument Object &000000007c4380e1000000004a99fb25 
() is not equal to DOMDocument Object &000000007c4380e6000000004a99fb25 ().

/home/lovely/Documents/php/test.php:16

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
    public function testPositiveTestcaseForassertXmlStringNotEqualsXmlString()
    { 
        $expectedxmlString  =  '<foo><bazx></bazx></foo>'; 
        $actualxmlString    =  '<foo><baz></baz></foo>';
        // Assert function to test whether given 
        // expected xml string is not equal to actual xml string
        $this->assertXmlStringNotEqualsXmlString(
            $actualxmlString,
            $expectedxmlString,
            "actual xml string is not equal to expected xml string"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                 1 / 1 (100%)

Time: 87 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)

```