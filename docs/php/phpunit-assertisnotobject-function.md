# PHPUnit assertIsNotObject()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisnotobject-function/](https://www.geeksforgeeks.org/phpunit-assertisnotobject-function/)

**assertIsNotObject()**函数是**PHPUnit**中的内置函数，用于断言实际给定的内容是否不存在对象。 如果实际给定的内容不是 Object，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertIsNotObject($actual[, $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Actual：**此参数可以是表示实际内容的任何类型。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertIsNotObject()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertIsNotObject() 
    { 
        $actualcontent = (object) ('lovely laptop');

        // Assert function to test whether given 
        // actual content is not object
        $this->assertIsNotObject(
            $actualcontent, 
            "actual content is not object"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                            1 / 1 (100%)

Time: 88 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeTestcaseForassertIsNotObject
actual content is not object
Failed asserting that stdClass Object &00000000469abe610000000023d4ee24 (
   'scalar' => 'lovely laptop'
) is not of type "object".

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
    public function testPositiveTestcaseForassertIsNotObject() 
    { 
        $actualcontent = ('lovely laptop');

        // Assert function to test whether given 
        // actual content is not object
        $this->assertIsNotObject(
            $actualcontent, 
            "actual content is not object"
        ); 
    } 
} 

?>
```

发帖主题：Re：Колибри0.7.0

```php
 PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                  1 / 1 (100%)

Time: 86 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)

```