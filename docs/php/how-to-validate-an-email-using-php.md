# 如何使用 PHP 验证电子邮件？

> 原文:[https://www . geesforgeks . org/如何使用-php 验证电子邮件/](https://www.geeksforgeeks.org/how-to-validate-an-email-using-php/)

本文包含用 PHP 验证电子邮件地址的不同方法。它使用正则表达式和内置的电子邮件验证功能。从用户处获取输入字符串，并将其与预定义的正则表达式进行匹配，如果发现正则表达式和输入字符串匹配，则返回 true 并继续。

**方法 1:** 使用正则表达式的电子邮件验证。

```php
<?php
// PHP program to validate email

// Function to validate email using regular expression
function email_validation($str) {
    return (!preg_match(
"^[_a-z0-9-]+(\.[_a-z0-9-]+)*@[a-z0-9-]+(\.[a-z0-9-]+)*(\.[a-z]{2,3})$^", $str))
        ? FALSE : TRUE;
}

// Function call
if(!email_validation("author@geeksforgeeks.com")) {
    echo "Invalid email address.";
}
else {
    echo "Valid email address.";
}

?>
```

**输出:**

```php
Valid email address.

```

**说明:**在上例中，将邮件传递给用户定义函数 *email_validation( $email )* ，该函数使用本例，并通过使用预定义函数 *preg_match()* 与正则表达式进行匹配。该预定义函数将整个输入与正则表达式匹配，如果匹配则返回真，否则返回假。

**方法 2:** 使用 filter_var()方法进行邮件验证。

```php
<?php

// Declare variable and initialize
// it to email
$email = "author@geeksforgeeks.com";

// Validate email
if (filter_var($email, FILTER_VALIDATE_EMAIL)) {
    echo("$email is a valid email address");
} 
else {
    echo("$email is not a valid email address");
}

?>
```

**Output:**

```php
author@geeksforgeeks.com is a valid email address

```

**说明:**在上例中，将输入的邮件地址传递给预定义函数 *filter_var()* ，该函数以两个参数作为输入邮件，第二个参数是邮件过滤器的类型。该功能过滤邮件并返回*真*或*假*。

**方法 3:** 使用 FILTER_SANITIZE_EMAIL 过滤器进行邮件验证。

```php
<?php

// Declare variable and store it to email
$email = "author.gfg@GeeksforGeeks.com";

// Remove all illegal characters from email
$email = filter_var($email, FILTER_SANITIZE_EMAIL);

// Validate Email
if (filter_var($email, FILTER_VALIDATE_EMAIL)) {
    echo("$email is a valid email address");
} 
else {
    echo("$email is not a valid email address");
}

?> 
```

**输出:**

```php
author.gfg@GeeksforGeeks.com is a valid email address

```

**说明:**在上面的示例中，使用 FILTER_SANITIZE_EMAIL 筛选器删除所有不支持的字符，然后使用 FILTER_VALIDATE_EMAIL 筛选器验证电子邮件。