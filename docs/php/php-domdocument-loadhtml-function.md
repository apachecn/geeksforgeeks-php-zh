# PHP|DOMDocument loadHTML()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-loadhtml-function/](https://www.geeksforgeeks.org/php-domdocument-loadhtml-function/)

**DOMDocument：：loadHTML()函数**是 PHP 中的内置函数，用于从字符串加载 HTML 文件。

**语法：**

```php
*bool* DOMDocument::loadHTML( *string* $source, *int* $options = 0 )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$source:** this parameter saves the HTML string.
*   **$Options:** this parameter is used to specify additional Libxml parameters in PHP 5.4.0 and Libxml 2.6.0.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。 如果静态调用此函数，则返回 DOMDocument，失败时返回 False。

**错误/异常：**如果将空字符串作为参数传递，则会生成警告消息。 此函数也可以静态调用，但它将发出 E_STRICT 错误。

下面的程序演示了 PHP 中的 DOMDocument：：loadHTML()函数：

**程序 1：**

```php
<?php

// Create a new DOMDocument
$doc = new DOMDocument();

// Load the HTML file
$doc->loadHTML(
"<html>
<head>
    <title>
        DOMDocument::loadHTML() function
    </title>
</head>
<body>
    <h1>GeeksforGeeks</h1>
    <h2>DOMDocument::loadHTML() function</h2>
</body>    
</html>");

// Creates an HTML document and display it
echo $doc->saveHTML();

?>
```

**输出：**

```php
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN"
        "http://www.w3.org/TR/REC-html40/loose.dtd">
<html>
<head>
    <title>
        DOMDocument::loadHTML() function
    </title>
</head>
<body>
    <h1>GeeksforGeeks</h1>
    <h2>DOMDocument::loadHTML() function</h2>
</body>
</html>

```

**程序 2：**

```php
<?php

// Create a new DOMDocument
$doc = new DOMDocument();

// Create an element
$comm1 = $doc->createComment('Starting of HTML document file');

// Append element to the document
$doc->appendChild($comm1);

// Creates an HTML document and display it
echo $doc->saveHTML();

// Load the HTML element to the document
$doc->loadHTML(
"<html>
<head>
    <title>PHP function</title>
</head>
<body>
    <h1>Welcome to GeeksforGeeks</h1>
    <h2>PHP function</h2>
    <div>A computer science portal</div>
</body>    
</html>");

// Create an element
$comm2 = $doc->createComment('Ending of HTML document file');

// Append element to the document
$doc->appendChild($comm2);

// Creates an HTML document and display it
echo $doc->saveHTML();

?>
```

**输出：**

```php
<!--Starting of HTML document file-->
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN" 
        "http://www.w3.org/TR/REC-html40/loose.dtd">
<html>
<head>
    <title>PHP function</title>
</head>
<body>
    <h1>Welcome to GeeksforGeeks</h1>
    <h2>PHP function</h2>
    <div>A computer science portal</div>
</body>
</html>
<!--Ending of HTML document file-->

```

**引用：**[https://www.php.net/manual/en/domdocument.loadhtml.php](https://www.php.net/manual/en/domdocument.loadhtml.php)