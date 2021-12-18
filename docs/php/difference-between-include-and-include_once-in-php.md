# PHP 中 include()和 include_once()的区别

> 原文:[https://www . geesforgeks . org/include 和 include _ in-PHP 的区别/](https://www.geeksforgeeks.org/difference-between-include-and-include_once-in-php/)

PHP 中的 [**include()**](https://www.geeksforgeeks.org/php-inclusion/) 函数主要用于将一个 PHP 文件的代码/数据包含到另一个文件中。在此过程中，如果有任何类型的错误，那么这个 require()函数将显示/给出警告，但是与执行停止的 [**require()**](https://www.geeksforgeeks.org/php-include-and-require/) 函数不同的是， **include()** 函数不会停止脚本的执行，而是脚本将继续其过程。

为了使用 **include()** 函数，我们首先需要创建两个 PHP 文件。然后使用 include()函数将一个 PHP 文件放入另一个文件中。之后，您将看到两个 PHP 文件合并成一个 HTML 文件。此 **include()** 不会查看该代码是否已经包含在指定文件中，而是会包含使用 **include()** 的代码次数。

**示例:**假设我们有一个名为*includegfg.php 的文件。*

## includegfg.php

```
<?php
   echo "
<p>Visit Again; " . date("Y") . " Geeks for geeks.com</p>
";
?>
```

我们已经创建了一个文件演示*。php* 。使用 **include()** 方法，我们将把*includegfg.php*文件包含到演示*中。php* 文件。

## demo.php

```
<html>
<body>
  <h1>Welcome to geeks for geeks!</h1>
  <p>Myself, Gaurav Gandal</p>
  <p>Thank you</p>

  <?php 
    include 'includegfg.php';
  ?>
</body>
</html>
```

**输出:**

![](img/a599b9654dfd2036d329bf468fe9dd13.png)

**include_once():**

PHP 中的[**include _ once()**](https://www.geeksforgeeks.org/php-include_once-require_once/)**函数主要用于将一个 PHP 文件包含到另一个 PHP 文件中。它为我们提供了一个特性，如果一个 PHP 文件中的代码已经包含在一个指定的文件中，那么它将不再包含该代码。这意味着这个函数只会将一个文件添加到另一个文件中一次。如果这个函数找到一个错误，那么它将产生一个警告，但不会停止执行。**

**如果*ABC.php*文件使用 **include_once()** 调用*XYZ.php*文件，并且出现任何错误，那么它将产生警告，但是不会停止脚本执行。**

****示例:**下面我们创建了一个名为*demo.php*的示例 PHP 文件，其中显示了消息“极客们，大家好”**

## **demo.php**

```
<?php
   echo "Hello from Geeks for Geeks";
?>
```

**在下面的 PHP 文件 *require_once_demo.php* 中，我们已经使用 [require_once()](https://www.geeksforgeeks.org/php-include_once-require_once/) 调用了*demo.php*文件两次，但是它不会执行第二次调用。**

## **require_once_demo.php**

```
<?php
   include_once('demo.php');
   include_once('demo.php');
?>
```

****输出:****

**![](img/1571cbeee27d89f0f8bead956d38a3e0.png)**

****include()和 include_once()的区别:****

<figure class="table">

| **包括()** | **包含 _ once()** |
| **The include () function is used to include one PHP file into another file, regardless of whether the file was previously included.** | **include _ once()** It will first check whether the file is already included, and if it is already included, it will not be included again. |
| This **include ()** function is mainly used in places where you want to include a certain code again and again. | This **include _ once ()** function is mainly used where you want to include a certain code only once. |
| **Include ()** The function will be executed every time it is called in the program. | **Include _ once ()** The function will not be executed every time it is called (that is. If the file to be included is previously included, it will not be executed) |
| In most cases, **contains ()** function for loading optional template class files. | Most **include _ once ()** functions are used to load optional dependencies (classes, functions, constants). |

</figure>