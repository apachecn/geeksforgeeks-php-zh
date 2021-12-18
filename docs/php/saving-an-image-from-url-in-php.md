# 在 PHP 中从网址保存图像

> 原文:[https://www . geeksforgeeks . org/从 php 中的 url 保存图像/](https://www.geeksforgeeks.org/saving-an-image-from-url-in-php/)

有时，需要从特定的网址下载一个图像，并将其用于项目中。很容易进入页面，使用右键按钮保存图像。但是如果你想通过编程来实现呢？原因可能因人而异，因开发者而异。如果集合了几百个给定的图像 URL 并且不知何故想要将它们保存到机器中，还是需要将这个概念运用到项目中。那么肯定不会手动下载这些文件。

从网址下载图片有两种不同的方法，如下所示:

*   Use basic file processing.
*   Use an HTTP library named cURL.

这两种方法都有各自的优缺点。

**使用基本文件处理:**这是完成任务最基本、最简单的方法。就像任何其他文件一样，从创建一个空文件开始，并以“写”模式打开它。之后，从源网址获取内容并粘贴到这个文件中。这听起来很简单。

从脚本中，你可以自己弄清楚它是做什么的。

*   声明两个名为 **$url** 和 **$img** 的变量，分别表示源 url 和目标文件。
*   使用 **file_put_contents()** 函数将字符串写入一个包含两个参数的文件。一个是文件名(或路径)，另一个是该文件的内容。
*   使用 **file_get_contents()** 函数将文件读入字符串。

**例:**

```php
<?php

$url = 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-6-1.png'; 

$img = 'logo.png'; 

// Function to write image into file
file_put_contents($img, file_get_contents($url));

echo "File downloaded!"

?>
```

```php
File downloaded!
```

**注意:**它会将图像保存到给定名称为 logo.png 的服务器上。

现在这个方法唯一的问题是它需要设置 allow_url_fopen 配置，默认情况下设置为 1。但是有时候，项目需求不允许有这个选项。这可能是因为一些预防性的安全措施，或者只是一个设计原则。在这种情况下，还有另一种保存图像的方法。

**使用 HTTP 库，cURL:** 严格来说，cURL 不仅仅是一个 HTTP 库。它还有其他几种数据传输协议。由于我们的图像在一个 HTTP 服务器上，我们将自己限制在这个库的这个小部分。

cURL 允许用 PHP 进行 HTTP 请求。首先初始化它的一个实例，并为请求设置一些必要的选项，包括 URL 本身。然后执行这个查询，返回文件的内容。之后，剩下的程序都是一样的。我们一拿到数据，就把它存到文件里。

**方法:**

*   In this script, we define a function **file _ get _ contents _ curl** to copy the behavior of **file _ get _ contents** from the aforementioned technology.
*   In this function, we have used the [T0】 CURR _ init 【T1] function to initialize an instance of CURR so as to use it to obtain data.
*   之后，需要使用**curl _ setup**设置一些选项，这样这个特殊的例子才能工作。该函数取三个参数
    *   An instance of cURL
    *   Corresponding options to be set
    *   And the value set by this option.

    在本例中，设置了以下选项:

    *   CURLOPT_HEADER, which is used to ensure whether a receiving header is needed;
    *   CURLOPT _ return transfer, which transmits data as the return value of **curl _ exec** function, instead of directly outputting it.
    *   There is another option, CURLOPT_URL, to set the URL for the request.
*   After that, we get the data from **curl _ exec** and return it from the parent function.
*   Then use **file _ put _ contents** to write the data into a file on the machine.

**例:**

```php
<?php

function file_get_contents_curl($url) {
    $ch = curl_init();

    curl_setopt($ch, CURLOPT_HEADER, 0);
    curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1);
    curl_setopt($ch, CURLOPT_URL, $url);

    $data = curl_exec($ch);
    curl_close($ch);

    return $data;
}

$data = file_get_contents_curl(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-6-1.png');

$fp = 'logo-1.png';

file_put_contents( $fp, $data );
echo "File downloaded!"

?>
```

**输出:**

```php
File downloaded!
```

这种方法在从互联网获取内容时提供了一点灵活性。如前所述，它不仅仅限于 HTTP，还可以用于许多其他情况。它允许以任何您想要的方式配置传输。例如 **file_get_contents** 使用简单的 get 请求来获取数据，但是使用 cURL，也可以使用 GET、POST、PUT 等方法。

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。