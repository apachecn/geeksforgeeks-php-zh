# PHP 中“=”短开标签是什么意思？

> 原文:[https://www . geeksforgeeks . org/short-open-tag-in-mean-PHP/](https://www.geeksforgeeks.org/what-does-short-open-tag-mean-in-php/)

**< php** 用于标识一个 php 文档的开始。

在 PHP 中，每当它读取一个 PHP 文档时，它都会查找:

```php
<?php ?>
```

它只处理上述标签之间的代码，而将其他代码留在它们周围。

**例如:**

```php
<?php
echo "Hello PHP !";
?>
```

**Output:**

```php
Hello PHP !

```