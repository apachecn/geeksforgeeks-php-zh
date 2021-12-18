# PHPUnit|assertDirectoryIsReadable()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertdirectoryisreadable-function/](https://www.geeksforgeeks.org/phpunit-assertdirectoryisreadable-function/)

**assertDirectoryIsReadable()**函数是 PHPUnit 中的内置函数，用于断言指定的目录是目录还是可读目录。 如果给定的目录路径存在且可读，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertDirectoryIsReadable( integer $directory, string $message = '' )

```

**参数：**此函数接受两个参数，如上面的语法所示。 参数描述如下：

*   **$DIRECTORY:** this parameter is a string that represents the directory path.
*   **$Message:** this parameter accepts string values. When the test case fails, the string message is displayed as an error message.

以下程序说明了 PHPUnit 中的 assertDirectoryIsReadable()函数：

**程序 1：**

```
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testNegativeTestcaseForAssertDirectoryIsReadable()
    {
        $directoryPath = "/home/shivam/Documents/phpunit/notreadable";

        // Assert function to test whether the given
        // directory path either exists and readable
        $this->assertDirectoryIsReadable(
            $directoryPath,
            "directoryPath  exists and readable"
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
    public function testPositiveTestcaseForAssertDirectoryIsReadable()
    {
        $directoryPath = "/home/shivam/Documents/geeks";

        // Assert function to test whether given
        // directory path exists and readable
        $this->assertDirectoryIsReadable(
            $directoryPath,
            "directoryPath exists and readable"
        );
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**要使用 phpunit 运行测试用例，请执行此处[中的步骤](https://www.jetbrains.com/help/phpstorm/using-phpunit-framework.html)。 此外，phpunit 7 及更高版本支持 assertDirectoryIsReadable()。