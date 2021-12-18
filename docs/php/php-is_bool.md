# PHP|is_bool()

> Original: [https://www.geeksforgeeks.org/php-is_bool/](https://www.geeksforgeeks.org/php-is_bool/)

is_bool()是 php 中的内置函数。 函数的作用是：确定变量是否为布尔值。

**语法**：

```php
boolean is_bool($variable_name)
$variable_name:the variable we want to check.
```

**返回值**：它是一个布尔函数，因此当$VARIABLE_NAME 为布尔值时返回 TRUE，否则返回 FALSE。

**示例 1**：

```php
<?php
//php code
$variable_name1 = false;
$variable_name2 = 32;

//$variable_name1 is boolean, gives TRUE
if (is_bool($variable_name1))

echo "Variable is a boolean. \n";
else
echo 'Variable is not a boolean. \n';

//$variable_name2 is boolean, gives FALSE
if (is_bool($variable_name2))

echo '32 is a boolean.\n';
else
echo '32 is not a boolean.';
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
Variable is a boolean. 
32 is not a boolean.

```

**示例 2**：

```php
<?php
// PHP code
function square($num)
{
    return (is_bool($num));
}
echo square(TRUE) ."\n";   // outputs '1'.
echo square(FALSE) ."\n";   // outputs '1'.
echo square(56) ."\n";   // nothing is returned.

?>
```

发帖主题：Re：Колибри0.7.8.0

```php
1
1

```

**参考**：[http://php.net/manual/en/function.is-bool.php](http://php.net/manual/en/function.is-bool.php)