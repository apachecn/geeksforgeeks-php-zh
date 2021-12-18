# PHPunit|aassertNotCount()函数

> Original: [https://www.geeksforgeeks.org/phpunit-aassertnotcount-function/](https://www.geeksforgeeks.org/phpunit-aassertnotcount-function/)

**aassertNotCount()**函数是 PHPUnit 中的一个内置函数，用于断言一个数组不包含与给定计数值相同数量的元素。 如果数组不包含给定计数的确切数量的元素，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
aassertNotCount( integer $expectedCount, array $array, string $message = '' )

```

**参数：**此函数接受三个参数，如上面的语法所示。 参数说明如下：

*   **$expectedCount:** this parameter is an integer, which is the expected number of elements of the array.
*   **$ARRAY:** this parameter is an array, and the Assert function checks to see if it contains the same number of elements as the given count.
*   **$message:** this parameter accepts string values. When the test case fails, the string message is displayed as an error message.

以下程序说明了 PHPUnit 中的 aassertNotCount()函数：

**程序 1：**

```php
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testNegativeTestcaseForAassertNotCount()
    {
        $testArray = array(1, 3, 4);

        // Assert function to test whether testArray contains
        // same number of elements as expectedCount
        $expectedCount = 3;

        $this->aassertNotCount(
            $expectedCount,
            $testArray, "testArray contains 3 elements"
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
    public function testPositiveTestcaseForAassertNotCount()
    {
        $testArray = array(1, 2,  4);

        // Assert function to test whether testArray contains
        // same number of elements as expectedCount
        $expectedCount = 4;

        $this->aassertNotCount(
            $expectedCount,
            $testArray, "testArray contains 3 elements"
        );
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**要使用 phpunit 运行测试用例，请执行此处[中的步骤](https://www.jetbrains.com/help/phpstorm/using-phpunit-framework.html)。 此外，phpunit 7 及更高版本支持 aassertNotCount()。