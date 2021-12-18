# PHP TRIGGER_ERROR()函数

> Original: [https://www.geeksforgeeks.org/php-trigger_error-function/](https://www.geeksforgeeks.org/php-trigger_error-function/)

**TRIGGER_ERROR()函数**是 PHP 中的内置函数，可以充当内置错误处理程序。 此函数通常由程序员用来触发或生成用户级错误、通知或消息。 它返回一个布尔值，即在表达式成功时返回 TRUE，在表达式失败时返回 FALSE。

**语法：**

```php
*bool* trigger_error(*string* $message, *int* $error_level);
```

这里，**$MESSAGE**参数是要显示的消息，它是字符串类型，而**$ERROR_LEVE**l 用于描述必须显示的错误类型，它是整型的。 对于任何 TRIGGER_ERROR()函数，$MESSAGE 是必需的，$ERROR_LEVEL 可以是可选的，具体取决于用户要求，$MESSAGE 的最大长度为 1024 字节。

**示例 1：**在此示例中，用户定义的函数**doFunction($var)**接受一个值作为该函数内部的参数。如果该值将是数值，则将检查该参数，然后将打印**$var。“is numeric”**，否则将抛出错误消息**“Variable Me Numic”**，这是通过 TRIGGER_ERROR()函数完成的。

## PHP

```php
<?php

function doFunction($var) {
    if(is_numeric($var)) {
        echo $var.' is numeric';
    } 
      else {
        trigger_error('variable must be numeric');
    }
}

$new_var = 'GFG';
doFunction($new_var);

?>
```

发帖主题：Re：Колибри0.7.0

```php
PHP Notice:  variable must be numeric in 
/home/d87c8897dcede28086b7e4f06f5fafc7.php on line 9\
```

**示例 2：**默认情况下，使用 TRIGGER_ERROR()函数将生成 PHP 通知，但是用户也可以通过在 TRIGGER_ERROR()函数中添加参数来生成 PHP 错误或 PHP 警告，如下例所示。

在本例中，我们创建了一个带有两个参数的 Divide 函数，如果**$Second**的值等于零，则 TRIGGER_ERROR()函数将抛出 PHP 致命错误，因为在参数**E_USER_ERROR**中，与错误消息一起传递给 TRIGGER_ERROR()，如果$Second 的值不等于零，则$First 将除以$Second 并显示结果。

## PHP

```php
<?php

function divide($first,$second) {

    if ($second == 0) {
        trigger_error("Cannot divide by zero", E_USER_ERROR);
      }
      else {
        echo $first/$second ;    
      }
}

divide(2,0)

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.trigger-error.php](https://www.php.net/manual/en/function.trigger-error.php)