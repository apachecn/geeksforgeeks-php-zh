# PHPunit|assertNotEmpty()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertnotempty-function/](https://www.geeksforgeeks.org/phpunit-assertnotempty-function/)

**assertNotEmpty()**函数是 PHPUnit 中的内置函数，用于断言指定的数据持有者是否是非空的。 如果提供的数据持有者非空，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertNotEmpty( mixed $dataHolder, string $message = '' )

```

**参数：**此函数接受两个参数，如上面的语法所示。 参数描述如下：

*   **$dataHolder:** this parameter can be any type that represents the holder of the data to be asserted.
*   **$Message:** this parameter accepts string values. When the test case fails, the string message is displayed as an error message.

以下程序说明了 PHPUnit 中的 assertNotEmpty()函数：

**程序 1：**

```
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testNegativeTestcaseForAssertNotEmpty()
    {
        $dataHolder = '';

        // Assert function to test whether given
        // data holder (variable) is non-empty or not
        $this->assertNotEmpty(
            $dataHolder,
            "data holder is empty"
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
    public function testPositiveTestcaseForAssertNotEmpty()
    {
        $dataHolder = 'test data';

        // Assert function to test whether given
        // data holder (variable) is non-empty or not
        $this->assertNotEmpty(
            $dataHolder,
            "data holder is empty"
        );
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**要使用 phpunit 运行测试用例，请执行此处[中的步骤](https://www.jetbrains.com/help/phpstorm/using-phpunit-framework.html)。 此外，phpunit 7 及更高版本也支持 assertNotEmpty()。