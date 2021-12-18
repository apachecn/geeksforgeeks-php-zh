# PHPUnit assertNan()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertnan-function/](https://www.geeksforgeeks.org/phpunit-assertnan-function/)

**assertNan()**函数是 PHPUnit 中的内置函数，用于断言变量是否为 NaN。 如果变量为 NaN，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertNan(mixed $variable[, string $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Variable:** this parameter represents any type of variable.
*   **$Message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的 assertNan()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertNan() 
    { 
        $variable = 0*0; 

        // Assert function to test whether given 
        // variable is (NAN) or not
        $this->assertNan(
          $variable,
          "variable is (NAN) or not"
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
    public function testPositiveTestcaseForassertNan() 
    { 
        $variable = NAN; 

        // Assert function to test whether given 
        // variable is (NAN) or not
        $this->assertNan(
          $variable,
          "variable is (NAN) or not"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertnan](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertnan)