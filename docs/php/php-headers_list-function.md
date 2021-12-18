# PHP|Headers_List()函数

> Original: [https://www.geeksforgeeks.org/php-headers_list-function/](https://www.geeksforgeeks.org/php-headers_list-function/)

Header_List()函数是 PHP 中的一个内置函数，它以数组的形式返回已发送或准备发送到客户端或浏览器的响应头的列表。

**语法：**

```php
array headers_list( void )
```

**参数：**此函数不接受任何参数。
**返回值：**它返回要发送到浏览器或客户端的标头列表或数组。

**注意：**它与 Headers_Sent()函数不同，后者适用于检查报头是否已发送，但 Headers_List()在此上下文中不适用，因为它列出了报头的已发送状态和准备发送状态。

**示例 1：**

```php
<?php

// Use setcookie() function to add
// response header
setcookie("cookie1", "value_of_cookie1");

// Define the header 
header("test: geeksforgeeks");

header("Content-type: text/plain");

// Display the array returned by the
// headers_list() function
print_r(headers_list());

?>
```

发帖主题：Re：Колибри0.7.0

```php
Array
(   
    [0] => Set-Cookie: cookie1=value_of_cookie1
    [1] => test: geeksforgeeks
    [2] => Content-type: text/plain;charset=UTF-8
)

```

**示例 2：**

```php
<?php

// Use setcookie() function to add 
// header automatically
setcookie('uid', 'user4059');

// Defining a custom response header
header("custom-res-header: cstm");

// Specifying plain text content in
// response
header('Content-type: text/plain');

// Display all sent headers
var_dump(headers_list());

?>
```

发帖主题：Re：Колибри0.7.0

```php
array(3) {
  [0]=>string(24) "Set-Cookie: uid=user4059"
  [1]=>string(23) "custom-res-header: cstm"
  [2]=>string(38) "Content-type: text/plain;charset=UTF-8"
}

```

**引用：**[http://php.net/manual/en/function.headers-list.php](http://php.net/manual/en/function.headers-list.php)