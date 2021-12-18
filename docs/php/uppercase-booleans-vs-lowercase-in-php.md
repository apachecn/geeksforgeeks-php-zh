# PHP 中大写布尔与小写

> 原文:[https://www . geesforgeks . org/大写-booleans-vs-小写-in-php/](https://www.geeksforgeeks.org/uppercase-booleans-vs-lowercase-in-php/)

布尔值表示真值。布尔值表示两种可能的值:真或假。可以给真值 1，给假值 0。

若要指定布尔文字，请使用常量“真”或“假”。两者都是*不区分大小写*。意思是真等于真，假等于假。所以它可以写成

```php
true === TRUE and false === FALSE
```

**示例 1:** 本示例显示大写和小写布尔值。

```php
<?php
// PHP program to illustrates
// boolean value

// Declare a variable and initialize it
$boolean = TRUE;

// Display the value of variable
echo $boolean . "\n";

// Declare a variable and initialize it
$boolean = true;

// Display the value of variable
echo $boolean;

?>
```

**Output:**

```php
1
1

```

**示例:**本示例比较大写和小写布尔值。

```php
<?php
// PHP program to illustrates
// boolean value

// Declare a variable and initialize it
$var1 = TRUE;
$var2 = true;

// Check both boolean value is same or not
if($var1 == $var2)
    echo "TRUE and true both are same \n";
else
    echo "TRUE and true both are different \n";

// Declare a variable and initialize it
$var1 = FALSE;
$var2 = false;

// Check both boolean value is same or not
if($var1 == $var2)
    echo "FALSE and false both are same \n";
else
    echo "FALSE and false both are different \n";
?>
```

**Output:**

```php
TRUE and true both are same 
FALSE and false both are same

```