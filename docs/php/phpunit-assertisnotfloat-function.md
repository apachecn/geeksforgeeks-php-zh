# PHPUnit assertIsNotFloat()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisnotfloat-function/](https://www.geeksforgeeks.org/phpunit-assertisnotfloat-function/)

**assertIsNotFloat()**函数是 PHPUnit 中的内置函数，用于断言实际获得的值是否不是浮点数。 如果实际值不是浮点型，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertIsNotFloat($actual[, $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Actual：**此参数可以是表示实际数据的任何类型的整数。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertIsNotFloat()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeForassertIsNotFloat()
    {    $actualvalue = (4.20);
        // Assert function to test whether actual 
        // value is float or not
        $this->assertIsNotFloat(

            $actualvalue, 
            "actual value is float or not"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                  1 / 1 (100%)

Time: 87 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeForassertIsNotFloat
actual value is float or not
Failed asserting that 4.2 is not of type "float".

/home/lovely/Documents/php/test.php:13

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
    public function testPositiveForassertIsNotFloat()
    {    $actualvalue = (420);
        // Assert function to test whether actual 
        // value is float or not
        $this->assertIsNotFloat(

            $actualvalue, 
            "actual value is float or not"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                1 / 1 (100%)

Time: 90 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)

```