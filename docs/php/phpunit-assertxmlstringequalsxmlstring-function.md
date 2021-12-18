# PHPUnit assertXmlStringEqualsXmlString()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertxmlstringequalsxmlstring-function/](https://www.geeksforgeeks.org/phpunit-assertxmlstringequalsxmlstring-function/)

**assertXmlStringEqualsXmlString()**函数是 PHPUnit 中的内置函数，用于断言实际的 XML 字符串是否等于预期的 XML 字符串。 如果期望的 XML 字符串与实际的 XML 字符串相同，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertXmlStringEqualsXmlString(string $expectedXml, 
string $actualXml[, string $message = ''])

```

**参数：**此函数接受上述三个参数，如下所述：

*   **$expectedXmlString:** this parameter can be any type that represents the expected XML string.
*   **$ActualXmlString:** this parameter can be any type that represents the actual XML string.
*   **$message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的 assertXmlStringEqualsXmlString()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertXmlStringEqualsXmlString()
    { 
        $expectedxmlString  =  '<foo><bazx></bazx></foo>'; 
        $actualxmlString    =  '<foo><baz></baz></foo>';
        // Assert function to test whether given 
        // expected xml string is equal to actual xml string
        $this->assertXmlStringEqualsXmlString(
            $actualxmlString,
            $expectedxmlString,
            "actual xml string is equal to expected xml string"
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
    public function testPositiveTestcaseForassertXmlStringEqualsXmlString()
    { 
        $expectedxmlString  =  '<foo><baz></baz></foo>'; 
        $actualxmlString    =  '<foo><baz></baz></foo>';
        // Assert function to test whether given 
        // expected xml string is equal to actual xml string
        $this->assertXmlStringEqualsXmlString(
            $actualxmlString,
            $expectedxmlString,
            "actual xml string is equal to expected xml string"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertxmlstringequalsxmlstring](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertxmlstringequalsxmlstring)