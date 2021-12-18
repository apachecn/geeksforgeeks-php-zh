# PHPUnit|assertStringNotContainsString()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertstringnotcontainsstring-function/](https://www.geeksforgeeks.org/phpunit-assertstringnotcontainsstring-function/)

**assertStringNotContainsString()**函数是 PHPUnit 中的内置函数，用于断言不包含子字符串的字符串。 如果字符串不包含子字符串，则此断言将返回 TRUE，否则将返回 FALSE，如果为 TRUE，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertStringNotContainsString(string $substring, string $string, string $message = ''])

```

**参数：**此函数接受三个参数，如上面的语法所示。 参数说明如下：

*   **$SUBSTRING:** this parameter represents the string to be a substring of a given string.
*   **$STRING:** this parameter is the string that the Assert function will check to see if it contains substrings.
*   **$message:** this parameter accepts string values. When the test case fails, the string message is displayed as an error message.

以下程序说明了 PHPUnit 中的 assertStringNotContainsString()函数：

**程序 1：**

```
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testNegativeTestcaseForAssertStringNotContainsString()
    {
        $testString = "geeksforgeek";
        $substring = "geeks"; 

        // Assert function to test whether 'geeks' is a 
        // substring of testString
        $this->assertStringNotContainsString($substring, $testString,
                          "testString  contains 'geeks' as substring") ;
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testPositiveTestcaseForAssertStringNotContainsString()
    {
        $testString = "geekforgeek";
        $substring = "geeks"; 

        // Assert function to test whether 'geeks' is a 
        // substring of testString
        $this->assertStringNotContainsString($substring, $testString, 
                        "testString contains 'geeks' as substring") ;
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**要使用 phpunit 运行测试用例，请执行此处[中的步骤](https://www.jetbrains.com/help/phpstorm/using-phpunit-framework.html)。 此外，phpunit 7 及更高版本支持 assertStringNotContainsString()。