# PHPUnit assertGreaterThan()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertgreaterthan-function/](https://www.geeksforgeeks.org/phpunit-assertgreaterthan-function/)

**assertGreaterThan()**函数是 PHPUnit 中的内置函数，用于断言实际值是否大于期望值。 如果实际值大于期望值，则此断言将返回 TRUE，否则返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertGreaterThan(mixed $expected, 
         mixed $actual[, string $message = ''])

```

**参数：**此函数接受三个参数，如上面的语法所示。 具体参数说明如下：

*   **$Expect：**此参数可以是表示预期数据的任何类型的数值。
*   **$Actual：**此参数可以是表示实际数据的任何类型的数值。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下程序说明了 PHPUnit 中的 assertGreaterThan()函数：

**程序 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertGreaterThan()
    {    $expected = 44; 
        $actual = 22;

        // Assert function to test whether expected 
        // value is greater than actual or not 
        $this->assertGreaterThan( 
            $expected, 
            $actual, 
            "actual value is not greater than expected"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

> 由 Sebastian Bergmann 和贡献者组成的 PHPUnit 8.5.8。
> 
> F 1/1(100%)
> 
> 时间：224ms，内存：10.00MB
> 
> 有一次失败：
> 
> 1)GeeksPhpunitTestCase：：testNegativeTestcaseForassertGreaterThan
> 实际值不大于预期
> 断言 22 大于 44 失败。
> 
> /home/loove/document/php/test.php：16
> 
> 失败！
> 测试：1，断言：1，失败：1。

**程序 2：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveTestcaseForassertGreaterThan()
    {    $expected = 22; 
        $actual = 44;

        // Assert function to test whether expected 
        // value is greater than actual or not 
        $this->assertGreaterThan( 
            $expected, 
            $actual, 
            "actual value is not greater than expected"
        ); 
    } 
} 

?> 
```

发帖主题：Re：Колибри0.7.0

```php
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                            1 / 1 (100%)

Time: 89 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)

```

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertgreaterthan](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertgreaterthan)