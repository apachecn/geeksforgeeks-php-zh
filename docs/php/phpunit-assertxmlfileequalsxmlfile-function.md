# PHPUnit assertXmlFileEqualsXmlFile()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertxmlfileequalsxmlfile-function/](https://www.geeksforgeeks.org/phpunit-assertxmlfileequalsxmlfile-function/)

**assertXmlFileEqualsXmlFile()**函数是 PHPUnit 中的一个内置函数，用于断言实际的 XML 文件内容是否等于预期的 XML 文件内容。 如果预期的 XML 文件内容与实际的 XML 文件内容相同，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertXmlFileEqualsXmlFile(string $expectedFile, 
string $actualFile[, string $message = ''])

```

**参数：**此函数接受三个参数，如上所述，如下所述：

*   **$expectedFile:** this parameter can be any type that represents the expected XML file path.
*   **$ActualFile:** this parameter can be any type that represents the actual XML file path.
*   **$Message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的 assertXmlFileEqualsXmlFile()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertXmlFileEqualsXmlFile()
    { 
        $actualFile =  '/home/lovely/Documents/php/actual.xml';
        $expectedFile     = '/home/lovely/Documents/php/expected.xml'; 

        // Assert function to test whether given 
        // expected xml file is equal to actual xml file or not
        $this->assertXmlFileEqualsXmlFile(
            $actualFile,
            $expectedFile, 
            "actual xml file equal to expected xml file or not"
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
    public function testPositiveTestcaseForassertXmlFileEqualsXmlFile()
    { 
        $actualFile =  '/home/lovely/Documents/php/actual.xml';
        $expectedFile    = '/home/lovely/Documents/php/expected.xml'; 
        // Assert function to test whether given 
        // expected xml file is equal to actual xml file or not
        $this->assertXmlFileEqualsXmlFile(
            $actualFile,
            $expectedFile, 
            "actual xml file equal to expected xml file or not"
        ); 
    } 
} 

?> 
```

**示例：**

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                 1 / 1 (100%)

Time: 87 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)

```

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertxmlfileequalsxmlfile](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertxmlfileequalsxmlfile)