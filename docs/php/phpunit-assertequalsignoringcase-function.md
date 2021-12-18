# PHPUnit assertEqualsIgnoringCase()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertequalsignoringcase-function/](https://www.geeksforgeeks.org/phpunit-assertequalsignoringcase-function/)

**assertEqualsIgnoringCase()**函数是 PHPUnit 中的内置函数，用于检查预期字符串是否等于实际字符串，而忽略预期字符串的字符串大小写。 如果实际字符串等于预期字符串(忽略区分大小写)，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertEqualsIgnoringCase(mixed $expected, 
      mixed $actual[, string $message = '']

```

**参数：**此函数接受三个参数，如上面的语法所示。 参数描述如下：

*   **$Expect:** this parameter is a string that represents the expected data.
*   $ **Actual:** this parameter is a string that represents the actual data.
*   **$message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下程序说明了 assertEqualsIgnoringCase()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForAssertequalIgnoringCase() 
    { 
        $expected = "Geek"; 
        $actual= "geEks";  
        // assert function to test whether expected string
        // is equal or not to actual ignoring case
        $this->assertEqualsIgnoringCase(
          $actual,
          $expected, 
          "expected is not equal to actual ignoring case") ; 
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
    public function testPositiveTestcaseForAssertequalIgnoringCase() 
    { 
        $expected = "Geeks"; 
        $actual= "geEks";  
        // assert function to test whether expected
        // is equal or not to actual ignoring case
        $this->assertEqualsIgnoringCase(
          $actual,
          $expected, 
          "expected is not equal to actual ignoring case") ; 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertequalsignoringcase](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertequalsignoringcase)