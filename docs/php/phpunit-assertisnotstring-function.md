# PHPUnit assertIsNotString()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisnotstring-function/](https://www.geeksforgeeks.org/phpunit-assertisnotstring-function/)

**assertIsNotString()**函数是 PHPUnit 中的内置函数，用于断言实际获取的值是否不是字符串值。 如果实际值不是字符串，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertIsNotString($actual[, $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$ActualValue：**此参数可以是表示实际数据的任何类型。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertIsNotString()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertIsNotString()
    {
        $actualvalue = "22"; 

        // Assert function to test whether given 
        // actualvalue is a string or not
        $this->assertIsNotString(
          $actualvalue,
          "actualvalue is a string or not"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                    1 / 1 (100%)

Time: 87 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeTestcaseForassertIsNotString
actualvalue is a string or not
Failed asserting that '22' is not of type "string".

/home/lovely/Documents/php/test.php:15

FAILURES!
Tests: 1, Assertions: 1, Failures: 1.

```

**示例 2：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveTestcaseForassertIsNotString()
    {
        $actualvalue = 420; 

        // Assert function to test whether given 
        // actualvalue is a string or not
        $this->assertIsNotString(
          $actualvalue,
          "actualvalue is a string or not"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                  1 / 1 (100%)

Time: 89 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)

```