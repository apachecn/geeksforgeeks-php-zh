# PHP|命名空间

> Original: [https://www.geeksforgeeks.org/php-namespace/](https://www.geeksforgeeks.org/php-namespace/)

与 C++一样，PHP 名称空间是封装项目的方式，因此可以重用相同的名称，而不会发生名称冲突。

*   在许多地方，它可以被视为一个抽象的概念。 它允许**在单独的名称空间中重新声明**相同的函数/类/接口/常量函数，而不会出现致命错误。
*   命名空间是包含常规 PHP 代码的分层标记的代码块。
*   命名空间可以包含有效的 PHP 代码。
*   命名空间影响以下类型的代码：类(包括抽象和特征)、接口、函数和常量。
*   命名空间是使用 NAMESPACE 关键字声明的。

命名空间必须在任何其他代码之前声明为文件顶部的命名空间-但有一个例外：DECLARE 关键字。

## PHP

```php
<?php
namespace MyNamespaceName {

    // Regular PHP code
    function hello()
    {
        echo 'Hello I am Running from a namespace!';
    }
}
?>
```

如果名称空间是全局声明的，则将其声明为**，而不使用**任何名称。

## PHP

```php
<?php
namespace {

    // Global space!
}
?>
```