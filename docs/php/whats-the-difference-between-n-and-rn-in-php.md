# PHP 中的\n 和\r\n 有什么区别？

> 原文:[https://www . geesforgeks . org/PHP 中的-n 和-rn 有什么区别/](https://www.geeksforgeeks.org/whats-the-difference-between-n-and-rn-in-php/)

PHP 中使用了许多类型的行尾字符。它们因操作系统和使用它们的编辑器而异。它还基于应用程序、库、协议和文件格式如何处理事情。这些角色是看不见的。 **\n** 用于换行符或换行符，而 **\r** 是回车符。它们的不同之处在于使用它们的方式，即语言依赖性成立。然而，跨平台的可移植性并不依赖于这些 EOL 字符的使用，这些字符可以通过使用 **PHP_EOL 常量**来维护。

*   **\r\n :**

    Windows 系统使用\r\n 作为行尾字符。因此，在 Windows 操作系统中，回车符是多余的。由于向后兼容，Windows 机器以双字符序列的形式输出换行符。此换行符在浏览器上不可见。为了在浏览器上可视化这些，可以在 PHP 中使用 [**nl2br()**](https://www.geeksforgeeks.org/php-nl2br-function/) 方法。但是，\n 也可以在 Windows 系统中使用。\r\n 是互联网上文本格式的标准行终止。\r\n 仅在 Windows 记事本、DOS 命令行、大多数 Windows 应用编程接口和一些(较旧的)Windows 应用程序中使用。

*   **\n:**

    UNIX 系统使用\n 作为行尾字符。此换行符在浏览器上不可见。\n 用于所有其他系统、应用程序和互联网。

> Linux/UNIX:\ n
> 
> **窗口:\r\n**

**PHP 代码:**下面的代码片段说明了行分隔符的用法。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
  #declaring a string
  $str = "Illustrating the usage \r\nof\n\rline\nseparators\r";
  #printing string
  echo nl2br($str);
?>
```

**Output**

```php
Illustrating the usage <br />
of<br />

line<br />
separators<br />
```

**说明:**两个行分隔符的功能在浏览器上是相同的。

以下是这些行尾字符的主要区别:

<figure class="table">

| **\ r \ n** | **\ n** |
| Compatible in windows-based systems. | Compatible in Unix/Linux-based systems. |
| Strictly for Linux system. | Can also be used for windows. |
| Also known as carriage return/line feed pair (CRLF). | Also known as standard disconnection. |
| It's a two-word literal sequence. | "\ n" is a character constant representing a single character, that is, a newline character. |

</figure>