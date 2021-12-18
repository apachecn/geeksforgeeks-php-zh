# 为什么 require_once()函数在 PHP 中使用起来那么糟糕？

> 原文:[https://www . geesforgeks . org/why-require _ once-function-once-so-bad-to-use-in-PHP/](https://www.geeksforgeeks.org/why-require_once-function-is-so-bad-to-use-in-php/)

**[require_once()函数](https://www.geeksforgeeks.org/php-include_once-require_once/)** 是 PHP 中的一个内置函数，如果我们想在另一个文件中包含一个 PHP 文件，即当我们需要在 PHP 脚本中包含一个文件不止一次时，这个函数非常有用。它用于检查文件是否包含多次，因为如果文件已经包含，它会在运行脚本时忽略所有包含。

**语法:**

```php
require_once('File name with file path');
```

**参数:**该函数接受单个参数‘带路径的文件名’。这是我们希望包含在 PHP 脚本中的文件。它是一个字符串类型的参数。

**返回值:**如果找到了被调用的文件，并且如果文件已经包含在内，那么函数将返回布尔型**真**，如果文件没有包含在内，那么函数将包含该文件并返回真。但是如果没有找到被调用的文件，那么将会出现一个致命的错误，并且不会显示任何输出，并且执行将停止返回布尔**假**。

下面的程序说明了 PHP 中的 require_once()函数:

**文件名:my_file.inc.php**

**程序:**

```php
<?php 

// Content of the PHP file
echo "Welcome To GeeksforGeeks"; 
?>
```

上面的文件 my_file.inc.php 在下面的文件 index.php 中包含了两次 require_once()函数。但是从输出中，您将忽略包含的第二个实例，因为 require_once()函数会忽略第一个实例之后的所有类似包含。

**文件名:index.php**

```php

<?php 

// Include the file

require_once('my_file.inc.php'); 
require_once('my_file.inc.php'); 

?> 
```

**输出:**

```php
Welcome To GeeksforGeeks
```

**为什么 require_once()函数这么不好用？**

*   require_once()函数在包含所有文件的同时给服务器带来了大量负载。
*   require_once()函数的功能在存储变量时用在重复函数内部时不合适。

**文件名:my_file.php**
**示例:**

```php

<?php 

// Content of the file
$var = 'GFG'; 

?>
```

**文件名:check.php**

```php
<?php

function func() {
    require_once('my_file.php');
    return $var;
}

for($i = 1; $i <= 3; $i++) {
    echo func() . "<br>";
}

?>
```

**输出:**

```php
GFG
```

通过用上述示例中的 require()函数替换 require_once()函数，我们可以确保变量`$var`在每次函数调用时都可用。

**文件名:check2.php**

```php
<?php

function func() {
    require('my_file.php');
    return $var;
}

for($i = 1; $i <= 3; $i++) {
    echo func() . "<br>";
}

?>
```

**输出:**

```php
GFG
GFG
GFG

```

require_once()函数比 require()或 include()函数慢，因为它会在每次脚本调用函数时检查文件是否已经包含在内。