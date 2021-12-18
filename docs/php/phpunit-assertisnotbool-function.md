# PHPUnit assertIsNotBool()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisnotbool-function/](https://www.geeksforgeeks.org/phpunit-assertisnotbool-function/)

**assertIsNotBool()**函数是 PHPUnit 中的内置函数，用于断言实际获取的值是否不是 Bool。 如果实际值为 Not a Bool，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertIsNotBool($actual[, $message = ''])

```

**参数：**此函数接受两个参数，如上面的语法所示。 具体参数说明如下：

*   **$ActualValue：**此参数可以是表示实际数据的任何类型。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertIsNotBool()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeForassertIsNotBooltrue()
    {    $actual = true;
        // Assert function to test whether actual 
        // value is (true or false) or not
        $this->assertIsNotBool( 

            $actual, 
            "actual value is bool or not"
        );

    }

    public function testNegativeForassertIsNotBoolFalse()
    {  
        $actual = False;
        // Assert function to test whether actual
        // value is (true or false) or not

        $this->assertIsNotBool( 

            $actual, 
            "actual value is bool or not"
        );
    }  
 } 
?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

FF                                                 2 / 2 (100%)

Time: 89 ms, Memory: 10.00 MB

There were 2 failures:

1) GeeksPhpunitTestCase::testNegativeForassertIsNotBooltrue
actual value is false/true
Failed asserting that true is not of type "bool".

/home/lovely/Documents/php/test.php:13

2) GeeksPhpunitTestCase::testNegativeForassertIsNotBoolFalse
actual value is false/true
Failed asserting that false is not of type "bool".

/home/lovely/Documents/php/test.php:29

FAILURES!
Tests: 2, Assertions: 2, Failures: 2.

```

**示例 2：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeForassertIsNotBooltrue()
    {    $actual = "true";
        // Assert function to test whether actual 
        // value is (true or false) or not
        $this->assertIsNotBool( 

            $actual, 
            "actual value is Bool or not"
        );

    }

    public function testNegativeForassertIsNotBoolFalse()
    {  
        $actual = "False";
        // Assert function to test whether actual
        // value is (true or false) or not

        $this->assertIsNotBool( 

            $actual, 
            "actual value is Bool or not"
        );
    }  
 } 
?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

..                                                2 / 2 (100%)

Time: 91 ms, Memory: 10.00 MB

OK (2 tests, 2 assertions)

```