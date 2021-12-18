# PHPUnit assertIsNotResource()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisnotresource-function/](https://www.geeksforgeeks.org/phpunit-assertisnotresource-function/)

**assertIsNotResource()**函数是 PHPUnit 中的内置函数，用于断言给定变量是否不是 Resource。 如果给定变量不是 Resource，则此断言将返回 TRUE，否则将返回 FALSE。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```
assertIsNotResource($actual[, $message = ''])

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Variable：**此参数可以是表示实际数据的任何类型的变量。
*   **$message：**此参数接受字符串值。 当测试用例失败时，此字符串消息显示为错误消息。

以下示例说明了 PHPUnit 中的 assertIsNotResource()函数：

**示例 1：**

## PHP

```
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertIsNotResource()
    { 
       $variable =  fopen('http://www.google.com','r');
        // Assert function to test whether assert
        //  variable is not resource
        $this->assertIsNotResource(
            $variable,
            "assert variable is not resource"
        );
       fclose($variable);
    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

F                                                  1 / 1 (100%)

Time: 759 ms, Memory: 10.00 MB

There was 1 failure:

1) GeeksPhpunitTestCase::testNegativeTestcaseForassertIsNotResource
assert variable is not resource
Failed asserting that resource(1227) of type (stream) is not of type "resource".

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
    public function testNegativeTestcaseForassertIsNotResource()
    { 
       $variable =  555;
        // Assert function to test whether assert
        //  variable is not resource
        $this->assertIsNotResource(
            $variable,
            "assert variable is not resource"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.0

```
PHPUnit 8.5.8 by Sebastian Bergmann and contributors.

.                                                  1 / 1 (100%)

Time: 88 ms, Memory: 10.00 MB

OK (1 test, 1 assertion)

```