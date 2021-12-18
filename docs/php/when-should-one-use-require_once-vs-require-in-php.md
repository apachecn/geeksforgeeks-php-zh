# 在 PHP 中什么时候应该使用 require_once() vs require()？

> 原文:[https://www . geesforgeks . org/when-one-use-require _ once-vs-require-in-PHP/](https://www.geeksforgeeks.org/when-should-one-use-require_once-vs-require-in-php/)

在这篇文章中，我们将学习，在 PHP 中什么时候应该使用[require _ once()](https://www.geeksforgeeks.org/php-include_once-require_once/)方法，什么时候使用 [require()](https://www.geeksforgeeks.org/php-inclusion/) 方法。

[****require()方法:****](https://www.geeksforgeeks.org/php-inclusion/) PHP require()是 PHP 中的一个库或内置函数。它通常用于我们想要在 PHP 代码或程序中包含一个文件的情况。如果找不到指定路径上的文件，require()方法将引发致命错误。如果出现任何错误，它也会停止内容的执行。通过使用 require()，用户可以在特定的 PHP 代码中任意多次包含一个文件。

**语法:**

```php
require('File_Name_With_Extension');
```

**示例:**下面的文件演示了 PHP require()方法。它包括下面给出的“welcome.html”文件内容。

## require.php

```php
<?php 

    require('welcome.html');
    require('welcome.html');

 ?>
```

以下是上述 PHP 代码中使用的文件“welcome.html”的内容。

## welcome.html

```php
<!DOCTYPE html>
<html>
  <body>
    <p>This file is included.</p>
  </body>
</html>
```

运行“require.php”文件后，会显示以下结果。

**输出:**

```php
This file is included.
This file is included.
```

[**require _ once():**](https://www.geeksforgeeks.org/php-include_once-require_once/)**PHP**require _ once()**也是 PHP 中的库函数。它也用于我们想要在 PHP 代码或程序中包含一个文件的情况。如果找不到指定路径上的文件，require_once()也会引发致命错误。如果出现任何错误，它还将停止内容的执行。通过使用 **require_once()，**用户可以在特定的 PHP 代码中包含一个 once 文件。**

****语法:****

```php
require_once('File_Name_With_Extension');
```

****示例:**在下面的示例中，我创建了两个文件，即“*welcome . html”*和“*require _ once . PHP”***。**两次调用 **require_once()** ，文件*“welcome . html”*只包含一次。**

## **require_once.php**

```php
<?php 
    require_once('welcome.html');   
    require_once('welcome.html');
 ?>
```

## **welcome.html**

```php
<!DOCTYPE html>
<html>
  <body>
    <p>This file is included only once!</p>
  </body>

</html>
```

**运行“require_once.php”文件后，会显示以下结果，**

****输出:****

```php
This file is included only once!
```

****require()和 require_once()的区别:****

<figure class="table">

| **require()** | **require _ once()** |
| With require (), the file can be included multiple times on the same web page. | By using require_once (), the file can only be included once on the web page. |
| Increase the loading time of web pages. | Web pages have the shortest loading time. |
| Increase the complexity of web pages. | Web pages have the least complexity. |

</figure>

****什么时候应该使用 require_once 而不是 require？****

*   ****require()** 包含文件，而不管该文件是否已经包含在网页中。因此，如果您想一次又一次地包含文件内容，并且只关心在网页上传递输出，可以使用 **require()** 。**
*   **而 **require_once()** 将只在网页上包含该文件一次，即使该函数被调用两次，它也将只执行一次，而忽略第二次函数调用，这将进一步导致加载时间和网页复杂性的最小化。因此，如果您关心输出的传递以及网页的加载时间和复杂性，那么您肯定应该使用 **require_once()** 。**