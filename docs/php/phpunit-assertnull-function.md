# PHPUnit assertNull()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertnull-function/](https://www.geeksforgeeks.org/phpunit-assertnull-function/)

**assertNull()**函数是 PHPUnit 中的内置函数，用于断言变量是否为空。 如果变量为空，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertNull(mixed $variable[, string $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Variable:** this parameter represents any type of variable.
*   **$Message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的参数 assertNull()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertNull() 
    { 
        $variable = "Null"; 

        // Assert function to test whether given 
        // variable is Null or not 
        $this->assertNull( 
            $variable, 
            "variable is null or not"
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
    public function testPositiveTestcaseForassertNull() 
    { 
        $variable = Null; 

        // Assert function to test whether given 
        // variable is Null or not 
        $this->assertNull( 
            $variable, 
            "variable is null or not"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertnull](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertnull)