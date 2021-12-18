# PHPUnit assertStringStartsWith()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertstringstartswith-function/](https://www.geeksforgeeks.org/phpunit-assertstringstartswith-function/)

**assertStringStartsWith()**函数是 PHPUnit 中的内置函数，用于断言实际字符串是否以预期的前缀字符串开头。 如果实际字符串以预期的前缀字符串开头，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertStringStartsWith(string $prefix, string $string
[, string $message = ''])

```

**参数：**此函数接受上述三个参数，如下所述：

*   **$expectedprefix:** this parameter can be any type that represents the expected prefix string.
*   **$ActualString:** this parameter can be any type that represents the actual string.
*   **$message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的 assertStringStartsWith()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertStringStartsWith()
    { 
        $expectedprefix = ('dis');
        $actualstring = ('agreedis');

        // Assert function to test whether 
        // actual string content starts with 
        // expected prefix string content or not
        $this->assertStringStartsWith(
            $expectedprefix,
            $actualstring, 
            "actual string content start with expected 
             prefix content or not"
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
    public function testPositiveTestcaseForassertStringStartsWith()
    { 
        $expectedprefix = ('dis');
        $actualstring = ('disagree');

        // Assert function to test whether 
        // actual string content starts with 
        // expected prefix string content or not
        $this->assertStringStartsWith(
            $expectedprefix,
            $actualstring, 
            "actual string content start with expected 
             prefix content or not"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertstringstartswith](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertstringstartswith)