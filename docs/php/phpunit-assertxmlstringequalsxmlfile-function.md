# PHPUnit assertXmlStringEqualsXmlFile()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertxmlstringequalsxmlfile-function/](https://www.geeksforgeeks.org/phpunit-assertxmlstringequalsxmlfile-function/)

**assertXmlStringEqualsXmlFile()**函数是 PHPUnit 中的内置函数，用于断言实际的 XML 文件内容是否等于预期的 XML 字符串。 如果预期的 XML 字符串与实际的 XML 文件内容相同，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertXmlStringEqualsXmlFile(string $expectedFile, 
string $actualFile[, string $message = ''])

```

**参数：**此函数接受三个参数，如上面的语法所示。 参数描述如下：

*   **and $expectedXmlString:** this parameter can be any type that represents the expected XML string.
*   **$ActualXmlFile:** this parameter can be any type that represents the actual XML file path.
*   **$message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

下面的示例说明了 PHPUnit 中的 assertXmlstring EqualsXmlFile()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertXmlStringEqualsXmlFile()
    { 
        $expectedxmlString  =  '<foo><baza></baza></foo>'; 
        $actualxmlFilePath    =  '/home/lovely/Documents/php/actual.xml';
        // Assert function to test whether given 
        // expected xml string is equal to actual xml file path
        $this->assertXmlStringEqualsXmlFile(
            $actualxmlFilePath,
            $expectedxmlString,
            "actual xml file path is equal to expected xml string"
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
    public function testPositiveTestcaseForassertXmlStringEqualsXmlFile()
    { 
        $expectedxmlString  =  '<foo><baz></baz></foo>'; 
        $actualxmlFilePath    =  '/home/lovely/Documents/php/actual.xml';
        // Assert function to test whether given 
        // expected xml string is equal to actual xml file path
        $this->assertXmlStringEqualsXmlFile(
            $actualxmlFilePath,
            $expectedxmlString,
            "actual xml file path is equal to expected xml string"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.8.0

**参考：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertxmlstringequalsxmlfile](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertxmlstringequalsxmlfile)