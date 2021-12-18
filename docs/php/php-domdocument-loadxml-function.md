# PHP|DOMDocument loadXML()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-loadxml-function/](https://www.geeksforgeeks.org/php-domdocument-loadxml-function/)

**DOMDocument：：loadXML()函数**是 PHP 中的一个内置函数，用于从字符串加载 XML 文件。

**语法：**

```
*mixed* DOMDocument::loadXML( *string* $source, *int* $options = 0 )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$source:** this parameter saves the string containing the XML document.
*   **$OPTIONS:** this parameter saves the bitwise OR of the libxml option constant.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。 如果静态调用此函数，则返回 DOMDocument，失败时返回 False。

下面的程序演示了 PHP 中的 DOMDocument：：loadXML()函数：

**程序 1：**

```
<?php

// Create a new DOMDocument
$doc = new DOMDocument();

// Load the XML file
$doc->loadXML(
"<user> 
    <username>Geeks123</username> 
    <name>GeeksforGeeks</name>  
    <address>  
        <phone>+91-XXXXXXXXXX</phone>
        <email>abc@geeksforgeeks.org</email>
    </address> 
</user>");

// Create XML file and display it
echo $doc->saveHTML();

?>
```

**输出：**

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

**程序 2：**

```
<?php

// Create new DOMDocument
$doc = new DOMDocument();

// Create a comment document
$comm1 = $doc->createComment('Starting of XML document');

// Append element to the document
$doc->appendChild($comm1);

// Create XML file and display it
echo $doc->saveHTML();

// Load the XML file
$doc->loadXML(
"<user> 
    <username>Geeks123</username> 
    <name>GeeksforGeeks</name>  
    <address>  
        <phone>+91-XXXXXXXXXX</phone>
        <email>abc@geeksforgeeks.org</email>
    </address> 
</user>");

// Create comment element
$comm2 = $doc->createComment('Ending of XML document');

// Append element to the document
$doc->appendChild($comm2);

// Create XML element and display it
echo $doc->saveHTML();

?>
```

**输出：**

```
<!--Starting of XML document-->
<user> 
    <username>Geeks123</username> 
    <name>GeeksforGeeks</name>  
    <address>  
        <phone>+91-XXXXXXXXXX</phone>
        <email>abc@geeksforgeeks.org</email>
    </address> 
</user><!--Ending of XML document-->

```

**引用：**[https://www.php.net/manual/en/domdocument.loadxml.php](https://www.php.net/manual/en/domdocument.loadxml.php)