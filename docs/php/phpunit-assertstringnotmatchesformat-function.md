# PHPUnit assertStringNotMatchesFormat()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertstringnotmatchesformat-function/](https://www.geeksforgeeks.org/phpunit-assertstringnotmatchesformat-function/)

**assertStringNotMatchesFormat()**函数是 PHPUnit 中的内置函数，用于断言给定字符串和给定格式之间的差异。 如果给定的字符串与格式类型不匹配，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertStringNotMatchesFormat(string $format, 
string $string[, string $message = ''])

```

**参数：**此函数接受三个参数，如上面的语法所示。 具体参数说明如下：

*   **$格式：**此参数表示为预先建立的数据布局。
*   **$string：**此参数可以是表示字符串的任何类型。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertStringNotMatchesFormat()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertStringNotMatchesFormat()
    { 
        $format =  "%d"; 
        $String  =  "420";

        // Assert function to test whether difference
        //between given string and type of format
        $this->assertStringNotMatchesFormat(
            $format,
            $String,
            " given string is not matched with 
              type of format"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                               1 / 1 (100%)

Time: 91 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeTestcaseForassertStringNotMatchesFormat
given string is not matched with type of formate
Failed asserting that string does not match format description.

/home/lovely/Documents/php/test.php:16

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
    public function testPositiveTestcaseForassertStringNotMatchesFormat()
    { 
        $format =  "%d"; 
        $String  =  "hh";

        // Assert function to test whether difference
        //between given string and type of format
        $this->assertStringNotMatchesFormat(
            $format,
            $String,
            " given string is not matched with 
              type of format"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                  1 / 1 (100%)

Time: 87 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)

```