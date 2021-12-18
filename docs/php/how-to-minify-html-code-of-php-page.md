# 如何缩小 PHP 页面的 HTML 代码？

> 原文:[https://www . geesforgeks . org/how-to-minify-html-code-of-PHP-page/](https://www.geeksforgeeks.org/how-to-minify-html-code-of-php-page/)

HTML 输出缩小对于通过减少页面加载时间和减少整体页面大小来提高网站性能非常重要。缩小 HTML 输出也减少了请求网站的用户的数据使用。
缩小可以通过去除不必要的细节，消除过多的空格、换行符、注释等来完成。然而，缩小会降低代码的可读性。缩小可以将文件大小减少 70%。PHP 用于将文件从开发环境传输到生产环境。HTML 文件可以手动和自动缩小。缩小可以使用几个在代码中添加空格的工具来撤销。但是，缩小过程中删除的任何注释都无法恢复。

**示例:**这是没有缩小代码的 HTML 文件。

```
<html>

<head>

<!-- This is the content that 
    shows in the browser tab -->

<title>Title Page</title>

</head>

<body>

<!-- This is a comment. -->

<h1>Hello world!</h1>
</body>

</html>
```

**缩小后的 HTML 文件**

> <title>扉页</title>
> 
> # 你好世界！

**方法 1:在 Apache 中使用 GZip 压缩:**

**在 Apache 中启用 Gzip 压缩的步骤**

1.  打开 Apache 配置文件

    ```
    vim /etc/httpd/conf/httpd.conf 
    ```

2.  检查配置文件中的以下行。

    ```
    LoadModule deflate_module modules/mod_deflate.so
    ```

3.  在配置文件的末尾添加以下几行。

    ```
    AddOutputFilterByType DEFLATE text/plain
    AddOutputFilterByType DEFLATE text/html
    AddOutputFilterByType DEFLATE text/xml
    AddOutputFilterByType DEFLATE text/css
    AddOutputFilterByType DEFLATE application/xml
    AddOutputFilterByType DEFLATE application/xhtml+xml
    AddOutputFilterByType DEFLATE application/rss+xml
    AddOutputFilterByType DEFLATE application/javascript
    AddOutputFilterByType DEFLATE application/x-javascript

    ```

4.  重启阿帕奇服务器

    ```
    sudo service httpd restart
    ```

**方法 2:** HTML 代码可以用带有回调的 ob_start()函数来缩小。

```
<?php
ob_start("minifier");
function minifier($code) {
    $search = array(

        // Remove whitespaces after tags
        '/\>[^\S ]+/s',

        // Remove whitespaces before tags
        '/[^\S ]+\</s',

        // Remove multiple whitespace sequences
        '/(\s)+/s',

        // Removes comments
        '/<!--(.|\s)*?-->/'
    );
    $replace = array('>', '<', '\\1');
    $code = preg_replace($search, $replace, $code);
    return $code;
}
?>
<!DOCTYPE html>
<html>

<head>

<!-- title of page -->

<title>Demo for minifier</title>

</head>

<body>

<!-- body of page -->

<h1>Hello World</h1>

</body>

</html>

<?php
ob_end_flush();
?>
```

**输出:**

> <title>Demo for minifier</title>
> 
> # Hello World

**方法 3:使用 HTMLMinifier 插件:** HTML Minifier 是一个服务器端源代码 Minifier，旨在通过删除不必要的空白、注释和换行符来优化发送给客户端的 HTML、CSS 和 JavaScript 输出。HTMLMinifier 在插件中提供了多种优化选项，可以根据用户需求进行选择。

**使用 HTMLMinifier 的步骤:**

1.  从*https://www.terresquall.com/download/HTMLMinifier.php*下载 HTMLMinifier 文件
2.  将以下代码包含到 php 文件

    ```
    <?php

    // Import the HTMLMinifier
    require_once 'myfolder/HTMLMinifier.php';

    // HTML source to be minified
    $htmlpage = file_get_contents('./mypage.html');

    // Minified version of the page
    echo HTMLMinifier::process($htmlpage);

    ?> 
    ```

3.  运行 php 文件