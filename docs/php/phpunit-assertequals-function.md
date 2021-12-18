# PHPunit|assertEquals()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertequals-function/](https://www.geeksforgeeks.org/phpunit-assertequals-function/)

**assertEquals()**函数是 PHPUnit 中的内置函数，用于断言实际获得的值是否等于期望值。 如果期望值与实际值相同，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertEquals( mixed $expected, mixed $actual, string $message = '' )

```

**参数：**此函数接受三个参数，如上面的语法所示。 参数描述如下：

*   **$Expect:** this parameter can be any type that represents the expected data.
*   **$Actual:** this parameter can be any type that represents the actual data.
*   **$message:** this parameter accepts string values. When the test case fails, the string message is displayed as an error message.

以下程序说明了 PHPUnit 中的 assertEquals()函数：

**程序 1：**

```
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testNegativeTestcaseForAssertEquals()
    {
        $expected = "geeks";
        $actual = "Geeks";

        // Assert function to test whether expected
        // value is equal to actual or not
        $this->assertEquals(
            $expected,
            $actual,
            "actual value is not equals to expected"
        );
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testPositiveTestcaseForAssertEquals()
    {
        $expected = "geeks";
        $actual = "geeks";

        // Assert function to test whether expected
        // value is equal to actual or not
        $this->assertEquals(
            $expected,
            $actual,
            "actual value is not equals to expected"
        );
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**要使用 phpunit 运行测试用例，请执行此处[中的步骤](https://www.jetbrains.com/help/phpstorm/using-phpunit-framework.html)。 此外，phpunit 7 及更高版本也支持 assertEquals()。