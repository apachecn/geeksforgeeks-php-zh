# PHPUnit assertIsArray()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisarray-function/](https://www.geeksforgeeks.org/phpunit-assertisarray-function/)

**assertIsArray()**函数是**PHPUnit**中的内置函数，用于断言给定变量是否为数组。 如果给定变量为数组，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertIsArray($actual[, $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Variable:** this parameter can be any type of variable that represents the actual data.
*   **$Message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

下面的示例说明了 PHPUnit 中的 assertIsArray()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeForassertIsArray()

    {  
     $variable  =  ("apple/banana");
        // Assert function to test whether assert
        //  variable is array or not
        $this->assertIsArray(
            $variable,
            "assert variable is array or not"
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
    public function testPositiveForassertIsArray()

    {  
     $variable  = array ("apple/banana");
        // Assert function to test whether assert
        //  variable is array or not
        $this->assertIsArray(
            $variable,
            "assert variable is array or not"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertisiterable](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertisiterable)