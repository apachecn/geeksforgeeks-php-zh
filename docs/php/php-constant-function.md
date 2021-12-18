# PHP 常量()函数

> 原文:[https://www.geeksforgeeks.org/php-constant-function/](https://www.geeksforgeeks.org/php-constant-function/)

**常量()**函数返回常量的值。它也适用于类常量。

**语法:**

```php
constant(constant)
```

**参数值:**

*   **Constant:** is a required option to specify a constant value.

**返回值:**如果定义了常量，则返回常量的值，否则返回空值。

**注意:**在 PHP 4.0 或更新版本上有效。

**异常:**如果未定义常数，则抛出 **E_WARNING** 错误**。**它发出运行时警告，不终止脚本。

下面是展示**常量()**函数工作的 PHP 程序。

**示例 1:区分大小写**

## PHP

```php
<?php

// Define a constant
define("Home","Welcome to GeeksforGeeks");

echo constant("Home");
?>
```

**输出:**

```php
Welcome to GeeksforGeeks
```

**示例 2:不区分大小写**

## PHP

```php
<?php

// Define a case insensitive constant
define("GFGConstant","True denotes case-insensitive", true);

echo constant("gfgconstant");
?>
```

**输出:**

```php
True denotes case-insensitive
```

**参考:**T2】https://www.php.net/manual/en/function.constant.php