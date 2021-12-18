# PHP 中数组()和[]的区别

> 原文:[https://www . geeksforgeeks . org/PHP 中数组与数组的区别/](https://www.geeksforgeeks.org/difference-between-array-and-in-php/)

可以使用 array()语言构造创建数组。它接受任意数量的逗号分隔的键= >值对作为参数。

**语法:**

```php
array(
    key  => value,
    key2 => value2,
    key3 => value3,
    ...
)

```

最后一个数组元素后的逗号不是必需的，可以省略，但这有助于其他开发人员了解数组是否更新。这通常针对单行数组，即数组(1，2)优于数组(1，2，.)。另一方面，对于多行数组，通常使用尾随逗号，因为这样可以更容易地在当前数组的末尾添加新元素。

**注意:**使用[]或 array()的唯一区别在于你使用的 PHP 版本。在 PHP 5.4 中，您还可以使用短数组语法，它将 array()替换为[]。

**例:**

```php
<?php

$array = array(
    "geek" => "tech",
    "tech" => "geek",
);

var_dump($array);

// As of PHP 5.4
$array = [
    "geek" => "tech",
    "tech" => "geek",
];

var_dump($array);
?>
```

**输出:**

```php
array(2) {
  ["geek"]=>
  string(4) "tech"
  ["tech"]=>
  string(4) "geek"
}
array(2) {
  ["geek"]=>
  string(4) "tech"
  ["tech"]=>
  string(4) "geek"
}

```