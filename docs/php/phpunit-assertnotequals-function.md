# PHPunit|assertNotEquals()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertnotequals-function/](https://www.geeksforgeeks.org/phpunit-assertnotequals-function/)

**assertNotEquals()**函数是 PHPUnit 中的内置函数，用于断言实际获得的值不等于预期值。 如果期望值不等于实际值，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertNotEquals( mixed $expected, mixed $actual, string $message = '' )

```

**参数：**此函数接受三个参数，如上面的语法所示。 参数描述如下：

*   **$Expect:** this parameter can be any type that represents the expected data.
*   **$Actual:** this parameter can be any type that represents the actual data.
*   **$message:** this parameter accepts string values. When the test case fails, the string message is displayed as an error message.

以下程序说明了 PHPUnit 中的 assertNotEquals()函数：

**程序 1：**

```php
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testNegativeTestcaseForAssertNotEquals()
    {
        $expected = "geeks";
        $actual = "geeks";

        // Assert function to test whether expected
        // value is unequal to actual or not
        $this->assertNotEquals(
            $expected,
            $actual,
            "actual value is equals to expected"
        );
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testPositiveTestcaseForAssertNotEquals()
    {
        $expected = "geeks";
        $actual = "Geeks";

        // Assert function to test whether expected
        // value is unequal to actual or not
        $this->assertNotEquals(
            $expected,
            $actual,
            "actual value is not equals to expected"
        );
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**要使用 phpunit 运行测试用例，请执行此处[中的步骤](https://www.jetbrains.com/help/phpstorm/using-phpunit-framework.html)。 此外，phpunit 7 及更高版本也支持 assertNotEquals()。