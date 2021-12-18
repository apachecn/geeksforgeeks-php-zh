# PHPUnit assertIsNotScalar()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisnotscalar-function/](https://www.geeksforgeeks.org/phpunit-assertisnotscalar-function/)

**assertIsNotScalar()**函数是 PHPUnit 中的内置函数，用于断言标量变量是包含整数、浮点数、字符串或布尔值的变量。 此函数不将 NULL 视为标量。 如果实际值是标量，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertIsNotScalar($actual[, $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Actual：**此参数可以是表示实际数据的任何类型的字符串或变量。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertIsNotScalar()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveForassertIsNotScalar()
    {   
     $actualvalue = "Null";
        // Assert function to test whether actual 
        // value is a any type of string or not
        $this->assertIsNotScalar(

            $actualvalue, 
            "actual value is a scalar or not"
        );

    }

     public function testNegativeForassertIsNotScalar()
    {   
     $actualvalue = 420;
            // Assert function to test whether actual 
        // value is a integer or not
        $this->assertIsNotScalar(

            $actualvalue, 
            "actual value is a scalar or not"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

FF                                                 2 / 2 (100%)

Time: 90 ms, Memory: 10.00 MB

There were 2 failures:

1) GeeksPhpunitTestCase::testPositiveForassertIsNotScalar
actual value is a scalar or not
Failed asserting that 'Null' is not of type "scalar".

/home/lovely/Documents/php/test.php:15

2) GeeksPhpunitTestCase::testNegativeForassertIsNotScalar
actual value is a scalar or not
Failed asserting that 420 is not of type "scalar".

/home/lovely/Documents/php/test.php:29

FAILURES!
Tests: 2, Assertions: 2, Failures: 2.

```

**程序 2：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveForassertIsNotScalar()
    {   
     $actualvalue = Null;
        // Assert function to test whether actual 
        // value is a any type of string or not
        $this->assertIsNotScalar(

            $actualvalue, 
            "actual value is a scalar or not"
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