# PHPUnit assert 无限()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertinfinite-function/](https://www.geeksforgeeks.org/phpunit-assertinfinite-function/)

**assert 无限()**函数是**PHPUnit**中的内置函数，用于断言实际获得的值是否为 INF。 如果实际值为 INF，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertInfinite(mixed $variable[, string $message = ''])

```

**参数：**此函数接受两个参数，如下所述：

*   **$ActualVariable:** this parameter can be any type of variable that represents the actual value.
*   **$Message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

下面的示例说明了 PHPUnit 中的 assertInfinite()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeForassertInfinite()

    {    
     $actualvariable = 1;
        // Assert function to test whether actual 
        // variable is INF or not
        $this->assertInfinite(
            $actualvariable, 
            "actual variable is INF or not"
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
    public function testPositiveForassertInfinite()

    {    
     $actualvariable = INF;
        // Assert function to test whether actual 
        // variable is INF or not
        $this->assertInfinite(
            $actualvariable, 
            "actual variable is INF or not"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertinfinite](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertinfinite)