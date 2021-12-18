# PHP|XMLWriter startCdata()函数

> Original: [https://www.geeksforgeeks.org/php-xmlwriter-startcdata-function/](https://www.geeksforgeeks.org/php-xmlwriter-startcdata-function/)

**XMLWriter：：startCdata()函数**是 PHP 中的一个内置函数，用于启动 CDATA。 然后需要使用*XMLWriter：：endCdata()*函数关闭该元素。 CDATA 是解析器不解析但被识别为标记的文本块。

**语法：**

```
*bool* XMLWriter::startCdata( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明了 PHP 中的**XMLWriter：：startCdata()函数**：

**示例 1：**

```
<?php

// Create a new XMLWriter instance
$writer = new XMLWriter();

// Create the output stream as PHP
$writer->openURI('php://output');

// Start the document
$writer->startDocument('1.0', 'UTF-8');

// Start a element
$writer->startElement('h1');

// Start the Cdata
$writer->startCdata();

// Add value to the Cdata
$writer->text('value');

// End the Cdata
$writer->endCdata();

// End the element
$writer->endElement();

// End the document
$writer->endDocument();
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```
<?php

// Create a new XMLWriter instance
$writer = new XMLWriter();

// Create the output stream as PHP
$writer->openURI('php://output');

// Start the document
$writer->startDocument('1.0', 'UTF-8');

// Start a element
$writer->startElement('p');

// Start the Cdata
$writer->startCdata();

// Add value to the Cdata which is not
// going to be visible on the webpage
$writer->text('This will be secret text, 
                 not visible in browser');

// End the Cdata
$writer->endCdata();

// Add value to the element
$writer->text('GeeksforGeeks, portal for 
                       Computer Science.');

// End the element
$writer->endElement();

// End the document
$writer->endDocument();
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.xmlwriter-start-cdata.php](https://www.php.net/manual/en/function.xmlwriter-start-cdata.php)