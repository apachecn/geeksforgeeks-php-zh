# PHPUnit assertStringEndsWith()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertstringendswith-function/](https://www.geeksforgeeks.org/phpunit-assertstringendswith-function/)

**assertStringEndsWith()**函数是 PHPUnit 中的内置函数，用于断言实际字符串是否以预期的后缀字符串结尾。 如果预期的后缀字符串以实际字符串结尾，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertStringEndsWith(string $suffix, string $string
[, string $message = ''])

```

**参数：**此函数接受三个参数，如上面的语法所示。 参数描述如下：

*   **$expectedSuffix:** this parameter can be any type that represents the expected suffix string.
*   **$ActualString:** this parameter can be any type that represents the actual string.
*   **$message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的 assertStringEndsWith()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertStringEndsWith()
    { 
        $expectedsuffix = ('thh');
        $actualstring = ('4th');

        // Assert function to test whether 
        // expected suffix string ends with
        // actual string content
        $this->assertStringEndsWith(
            $expectedsuffix,
            $actualstring, 
            "actual string content ends with expected 
             suffix content"
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
    public function testPositiveTestcaseForassertStringEndsWith()
    { 
        $expectedsuffix = ('th');
        $actualstring = ('4th');

        // Assert function to test whether 
        // expected suffix
        // string ends with actual string content
        $this->assertStringEndsWith(
            $expectedsuffix,
            $actualstring, 
            "actual string content ends with 
             expected suffix content"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertstringendswith](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertstringendswith)