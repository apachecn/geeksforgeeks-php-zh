# PHP|定义常量

> Original: [https://www.geeksforgeeks.org/php-defining-constants/](https://www.geeksforgeeks.org/php-defining-constants/)

在生产级代码中，将信息作为变量或常量保存，而不是显式使用它们，这一点非常重要。 PHP 常量只是一个简单值的标识符，它往往不会随着时间的推移而改变(例如网站的域名，例如。 Www.geeksforgeeks.org)。 理想的做法是将所有常量保存在单个 PHP 脚本中，这样维护起来更容易。 有效的常量名称必须以字母或下划线开头，并且不需要‘{content}#x2019；。 需要注意的是，常量与其作用域无关，即常量自动为全局作用域。
为了在 PHP 中创建常量，我们必须使用 Define()方法。

**语法：**

```php
bool define(identifier, value, case-insensitivity)
```

**参数**：该函数有两个必选参数和一个可选参数。

*   标识符：指定要分配给常量的名称。
*   值：指定要分配给常量的值。
*   不区分大小写(可选)：指定常量标识符是否应该不区分大小写。 默认情况下，它设置为 False，即区分大小写。

**返回类型**：此方法成功时返回 TRUE，失败时返回 FALSE。
下面是一些示例来说明 Define()函数的工作原理：

*   下面的程序说明了定义不区分大小写的常量：

## PHP

```php
<?php

  // case-insensitive constants
  define("Constant","Hello Geeks!",TRUE);
  echo constant;
  echo Constant;
?>
```

*   发帖主题：Re：Kolibrios

```php
Hello Geeks!  // Case Insensitive thus value is echoed
Hello Geeks!
```

*   下面的程序说明了如何定义区分大小写的常量：

## PHP

```php
<?php

  // case-sensitive constant
  define("Constant","Hello Geeks!");
  echo constant;
  echo Constant;
?>
```

*   发帖主题：Re：Kolibrios

```php
constant   // Case Sensitive thus value not echoed
Hello Geeks! 
```

*   PHP 编译器还将在输出的同时为上述程序抛出警告：“PHP 通知：在第 5 行使用未定义的常量常量-假定为‘常量’”。

**摘要**：

*   常量是可以赋值的标识符(字符串、布尔值、数组、整数、浮点数或 NULL)，通常不会随着时间的推移而改变。
*   常量与作用域无关，始终填充全局作用域。
*   定义()方法用于定义常量。
*   Defined()方法用于检查是否定义了常量。
*   Constant()方法用于返回常量的值，如果未定义常量，则返回 NULL。