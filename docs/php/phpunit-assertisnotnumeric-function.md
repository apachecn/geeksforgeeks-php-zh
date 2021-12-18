# PHPUnit assertIsNotNumeric()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisnotnumeric-function/](https://www.geeksforgeeks.org/phpunit-assertisnotnumeric-function/)

**assertIsNotNumeric()**函数是 PHPUnit 中的内置函数，用于断言给定的实际变量是否不是数字。 如果实际变量不是数字，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertIsNotNumeric($actual[, $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Actual：**此参数可以是表示实际数据的任何类型的变量。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

下面的示例说明了 PHPUnit 中的**assertIsNotNumeric()**函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeForassertIsNotNumeric()
    {   
     $actualvalue = "1111";
        // Assert function to test whether actual 
        // variable is numeric or not
        $this->assertIsNotNumeric(

            $actualvalue, 
            "actual value is Numeric or not"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                  1 / 1 (100%)

Time: 88 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeForassertIsNotNumeric
actual value is Numeric or not
Failed asserting that '1111' is not of type "numeric".

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
    public function testPositiveForassertIsNotNumeric()
    {   
     $actualvalue = "welcom";
            // Assert function to test whether actual 
        // variable is numeric or not
        $this->assertIsNotNumeric(

            $actualvalue, 
            "actual value is Numeric or not"
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