# PHPUnit assertIsNotIterable()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisnotiterable-function/](https://www.geeksforgeeks.org/phpunit-assertisnotiterable-function/)

**assertIsNotIterable()**函数是 PHPUnit 中的内置函数，用于断言给定变量是否不可迭代。 如果给定变量不是可迭代的，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertIsNotIterable($actual[, $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Variable：**此参数可以是表示实际数据的任何类型的变量。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertIsNotIterable()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertIsNotIterable()
    { 
       $variable = ([1, 2, 3]);
        // Assert function to test whether assert
        //  variable is Iterable
        $this->assertIsNotIterable(
            $variable,
            "assert variable is Iterable"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                      1 / 1 (100%)

Time: 88 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeTestcaseForassertIsNotIterable
assert variable is Iterable
Failed asserting that Array &0 (
  0 => 1
  1 => 2
  2 => 3
) is not of type "iterable".

/home/lovely/Documents/php/test.php:14

FAILURES!
Tests: 1, Assertions: 1, Failures: 1.

```

**示例 2：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveTestcaseForassertIsNotIterable()
    { 
       $variable = "[1, 2, 3]";
        // Assert function to test whether assert
        //  variable is Iterable
        $this->assertIsNotIterable(
            $variable,
            "assert variable is Iterable"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                 1 / 1 (100%)

Time: 86 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)

```