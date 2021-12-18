# PHP|DOMDocument loadHTMLFile()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-loadhtmlfile-function/](https://www.geeksforgeeks.org/php-domdocument-loadhtmlfile-function/)

**DOMDocument：：loadHTMLFile()函数**是 PHP 中的内置函数，用于从文件加载 HTML。

**语法：**

```
*bool* DOMDocument::loadHTMLFile( *string* $filename, *int* $options = 0 )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$filename:** this parameter saves the path of the HTML file.
*   **$Options:** this parameter is used to specify additional Libxml parameters in PHP 5.4.0 and Libxml 2.6.0.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。 如果静态调用此函数，则返回 DOMDocument，失败时返回 False。

下面的程序演示了 PHP 中的 DOMDocument：：loadHTMLFile()函数：

**gfg.html**

```
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
```

**程序 1：**

```
<?php

// Create a new DOMDocument
$doc = new DOMDocument();

// Load the HTML file
$doc->loadHTMLFile("gfg.html");

// Create an HTML document and display it
echo $doc->saveHTML();

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new DOMDocument
$doc = new DOMDocument();

// Create an element
$comm1 = $doc->createComment('Starting of HTML document file');

// Append element to the document
$doc->appendChild($comm1);

// Create an HTML document and display it
echo $doc->saveHTML();

// Load the HTML file
$doc->loadHTMLFile('gfg.html');

// Create an element
$comm2 = $doc->createComment('Ending of HTML document file');

// Append element to the document
$doc->appendChild($comm2);

// Create an HTML document and display it
echo $doc->saveHTML();

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domdocument.loadhtmlfile.php](https://www.php.net/manual/en/domdocument.loadhtmlfile.php)