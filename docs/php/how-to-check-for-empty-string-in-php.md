# PHP 中如何检查空字符串？

> 原文:[https://www . geesforgeks . org/如何在 php 中检查空字符串/](https://www.geeksforgeeks.org/how-to-check-for-empty-string-in-php/)

在本文中，我们将看到如何在 PHP 中检查空字符串。字符串是一组字符。如果字符串不包含任何字符，则称其为空。我们可以使用 [**空()**](https://www.geeksforgeeks.org/php-empty-function/) 功能来检查一个字符串是否为空。

函数用于检查字符串是否为空。如果字符串为空，它将返回 true。

**语法:**

```php
bool empty(string)
```

**参数:**变量，检查是否为空。

**返回值:**如果字符串为空，则返回真，否则返回假。

**例 1:** 检查字符串是否为空的 PHP 程序。

## PHP

```php
<?php

// Consider a string which is empty
$s = "";

// Return a message if string is empty
if(empty($s)) {
    echo "Empty string";
}
else {
    echo "Not empty";
}

?>
```

**输出**

```php
Empty string
```

**例 2:**

## PHP

```php
<?php

// Consider a string which is not empty
$s = "Welcome to GFG";

// Return a message if string is empty
if(empty($s)) {
    echo "Empty string";
}
else {
    echo "Not empty";
}

?>
```

**输出**

```php
Not empty
```