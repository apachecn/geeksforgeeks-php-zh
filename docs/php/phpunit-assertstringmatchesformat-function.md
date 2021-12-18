# PHPUnit assertStringMatchesFormat()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertstringmatchesformat-function/](https://www.geeksforgeeks.org/phpunit-assertstringmatchesformat-function/)

**assertStringMatchesFormat()**函数是 PHPUnit 中的内置函数，用于断言给定的字符串是否与格式匹配。 如果与 Format Else 类型匹配的给定字符串返回 False，则此断言将返回 True。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertStringMatchesFormat(string $format, string $string[, string $message = ''])

```

**参数：**此函数接受上述三个参数，如下所述：

*   **$format:** this parameter represents a pre-established layout for data.
*   **$STRING:** this parameter can be any type that represents a string.
*   **$message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的 assertStringMatchesFormat()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertStringMatchesFormat()
    { 
        $format =  "%d"; 
        $String  =  "hh";

        // Assert function to test whether given 
        // string is matched with type of format or not
        $this->assertStringMatchesFormat(
            $format,
            $String,
            " given string is matched with type 
              of format or not"
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
    public function testPositiveTestcaseForassertStringMatchesFormat()
    { 
        $format =  "%d"; 
        $String  =  "24";

        // Assert function to test whether given 
        // string is matched with type of format or not
        $this->assertStringMatchesFormat(
            $format,
            $String,
            " given string is matched with type 
              of format or not"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertstringmatchesformat](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertstringmatchesformat)