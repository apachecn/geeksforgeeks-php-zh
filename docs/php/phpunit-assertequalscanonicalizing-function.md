# PHPunit|assertEqualsCanonicalization()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertequalscanonicalizing-function/](https://www.geeksforgeeks.org/phpunit-assertequalscanonicalizing-function/)

**assertEqualsCanonicalization()**函数是 PHPUnit 中的内置函数，用于断言预期变量和实际变量是否规范相等。 规范相等意味着在实际比较之前，将对两个数组进行排序和比较。 如果 Expect 和 Actual 相同，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertEqualsCanonicalizing( mixed $expected, mixed $actual, string $message = '' )

```

**参数：**此函数接受三个参数，如上面的语法所示。 参数描述如下：

*   **$Expect:** this parameter is a mixed variable that represents the expected value.
*   **$Actual:** this parameter is a mixed variable that represents the actual value to be compared to the expected value.
*   **$message:** this parameter accepts string values. When the test case fails, the string message is displayed as an error message.

以下程序说明了 PHPUnit 中的 assertEqualsCanonicalization()函数：

**程序 1：**

```php
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testNegativeTestcaseForAssertEqualsCanonicalizing()
    {
        $expected = array(1, 2, 3, 4);
        $actual = array(2, 1, 2, 4);

        // Assert function to test whether expected 
        // and actual are canonically equal or not.
        $this->assertEqualsCanonicalizing(
            $expected, $actual, 
            "expected and actual are not canonically equals"
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
    public function testPositiveTestcaseForAssertEqualsCanonicalizing()
    {
         $expected = array(1, 2, 3, 4);
        $actual = array(2, 1, 3, 4);

        // Assert function to test whether expected 
        // and actual are canonically equal or not.
        $this->assertEqualsCanonicalizing(
            $expected, $actual, 
            "expected and actual are not canonically equals"
        );
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**要使用 phpunit 运行测试用例，请执行此处[中的步骤](https://www.jetbrains.com/help/phpstorm/using-phpunit-framework.html)。 此外，phpunit 7 及更高版本也支持 assertEqualsCanonicalization()。