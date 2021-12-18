# PHPUnit assertNotNull()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertnotnull-function/](https://www.geeksforgeeks.org/phpunit-assertnotnull-function/)

**assertNotNull()**函数是 PHPUnit 中的内置函数，用于断言变量是否不是(Null)。 如果变量不是(Null)，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertNotNull(mixed $variable[, string $message = ''])

```

**参数：**此函数接受两个参数，如下所述：

*   **$Variable：**此参数表示任何类型的变量。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的参数 assertNotNull()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertNotNull() 
    { 
        $variable = Null; 

        // Assert function to test whether given 
        // variable is null or not 
        $this->assertNotNull( 
            $variable, 
            "variable is null or not"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                  1 / 1 (100%)

Time: 86 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testPositiveTestcaseForassertNotNull
variable is null or not
Failed asserting that null is not null.

/home/lovely/Documents/php/test.php:15

FAILURES!
Tests: 1, Assertions: 1, Failures: 1.

```

**示例 2：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveTestcaseForassertNotNull() 
    { 
        $variable = "Null"; 

        // Assert function to test whether given 
        // variable is empty or not 
        $this->assertNotNull( 
            $variable, 
            "variable is null or not"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                  1 / 1 (100%)

Time: 88 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)

```