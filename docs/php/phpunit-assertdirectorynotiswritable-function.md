# PHPunit|assertDirectoryNotIsWritable()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertdirectorynotiswritable-function/](https://www.geeksforgeeks.org/phpunit-assertdirectorynotiswritable-function/)

**assertDirectoryNotIsWritable()**函数是 PHPUnit 中的内置函数，用于断言指定的目录不是目录还是不可写。 如果给定的目录路径不存在或不可写，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertDirectoryNotIsWritable( integer $directory, string $message = '' )

```

**参数：**此函数接受两个参数，如上面的语法所示。 参数描述如下：

*   **$DIRECTORY:** this parameter is a string that represents the directory path.
*   **$Message:** this parameter accepts string values. When the test case fails, the string message is displayed as an error message.

以下程序说明了 PHPUnit 中的 assertDirectoryNotIsWritable()函数：

**程序 1：**

```php
<?php
use PHPUnit\Framework\TestCase;

class GeeksPhpunitTestCase extends TestCase
{
    public function testNegativeTestcaseForassertDirectoryNotIsWritable()
    {
        $directoryPath = "/home/shivam/Documents/phpunit/notwritable";

        // Assert function to test whether given
        // directory path either doesn't exists or not writable
        $this->assertDirectoryNotIsWritable(
            $directoryPath,
            "directoryPath either doesn't exists or not writable"
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
    public function testPositiveTestcaseForAssertDirectoryNotIsWritable()
    {
        $directoryPath = "/home/shivam/Documents/geeks";

        // Assert function to test whether given
        // directory path exists or not writable
        $this->assertDirectoryNotIsWritable(
            $directoryPath,
            "directoryPath either doesn't exists or not writable"
        );
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**要使用 phpunit 运行测试用例，请执行此处[中的步骤](https://www.jetbrains.com/help/phpstorm/using-phpunit-framework.html)。 此外，phpunit 7 及更高版本支持 assertDirectoryNotIsWritable()。