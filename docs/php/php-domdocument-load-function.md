# PHP|DOMDocument load()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-load-function/](https://www.geeksforgeeks.org/php-domdocument-load-function/)

**DOMDocument：：Load()函数**是 PHP 中的一个内置函数，用于从文件加载 XML 文档。

**语法：**

```
*mixed* DOMDocument::load( *string* $filename, *int* $options = 0 )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$filename:** this parameter saves the path of the XML document.
*   **$OPTIONS:** this parameter saves the bitwise OR of the libxml option constant.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。 如果静态调用此函数，则返回 DOMDocument，失败时返回 False。

下面的程序演示了 PHP 中的 DOMDocument：：Load()函数：

**gfg.xml**

```
<user> 
    <username>Geeks123</username> 
    <name>GeeksforGeeks</name>  
    <address>  
        <phone>+91-XXXXXXXXXX</phone>
        <email>abc@geeksforgeeks.org</email>
    </address> 
</user> 
```

**程序：**

```
<?php

// Create a new DOMDocument
$doc = new DOMDocument();

// Load the XML file to the document
$doc->load('gfg.xml');

// Create a XML document and display it
echo $doc->saveXML();

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/domdocument.load.php](https://www.php.net/manual/en/domdocument.load.php)