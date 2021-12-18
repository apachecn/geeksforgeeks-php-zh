# PHPUnit assertIsResource()函数

> Original: [https://www.geeksforgeeks.org/phpunit-assertisresource-function/](https://www.geeksforgeeks.org/phpunit-assertisresource-function/)

AssertIsResource()函数是 PHPUnit 中的内置函数，用于断言给定变量是否为 Resource。 如果给定变量为 Resource，则此断言将返回 True，否则返回 False。 如果为 true，则断言的测试用例通过，否则测试用例失败。

**语法：**

```php
assertIsResource($actual[, $message = ''])

```

**参数：**此函数接受两个参数，如上所述：

*   **$Variable:** this parameter can be any type of variable that represents the actual data.
*   **$Message:** this parameter accepts string values. This string message is displayed as an error message when the test case fails.

以下示例说明了 PHPUnit 中的 assertIsResource()函数：

**示例 1：**

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testNegativeTestcaseForassertIsResource()
    { 
       $variable =  555;
        // Assert function to test whether assert
        //  variable is resource or not
        $this->assertIsResource(
            $variable,
            "assert variable is resource or not"
        );

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.8.0

示例 2：

## PHP

```php
<?php 
use PHPUnit\Framework\TestCase; 

class GeeksPhpunitTestCase extends TestCase 
{ 
    public function testPositiveTestcaseForassertIsResource()
    { 
       $variable =  fopen('http://www.google.com','r');
        // Assert function to test whether assert
        //  variable is Iterable
        $this->assertIsResource(
            $variable,
            "assert variable is Iterable or not"
        );
       fclose($variable);

    }

 } 
?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://phpunit.readthedocs.io/en/9.2/assertions.html#assertisresource](https://phpunit.readthedocs.io/en/9.2/assertions.html#assertisresource)