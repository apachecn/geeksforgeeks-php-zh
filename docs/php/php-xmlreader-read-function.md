# PHP|XMLReader read()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-read-function/](https://www.geeksforgeeks.org/php-xmlreader-read-function/)

**XMLReader：：Read()函数**是 PHP 中的一个内置函数，用于移动到文档中的下一个节点。 因此，该函数用于遍历 XML 文档。

**语法：**

```php
*bool* XMLReader::read( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序演示了 PHP 中的**XMLReader：：Read()函数**：

**程序 1：**在本程序中，我们将在遍历文件`data.xml`后获得元素的值

加入时间：清华大学 2007 年 01 月 25 日下午 3：33

**文件名：***index.php*

```php
<?php

// Create a new XMLReader instance
$XMLReader = new XMLReader();

// Open the XML file
$XMLReader->open('data.xml');

// Iterate through the XML nodes to
// reach the h1 element's text 
// (Only four times)
$XMLReader->read();
$XMLReader->read();
$XMLReader->read();
$XMLReader->read();

// Print the value of element
echo "The text inside is: "
    . "$XMLReader->value<br>";
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**在本程序中，我们将遍历一个元素后得到它的名称。

加入：清华 2007 年 01 月 25 日下午 3：33 发布时间：338

**文件名：***index.php*

```php
<?php

// Create a new XMLReader instance
$XMLReader = new XMLReader();

// Open the XML file
$XMLReader->open('data.xml');

// Iterate through the XML nodes
// to reach the h1 element
// (only three times)
$XMLReader->read();
$XMLReader->read();
$XMLReader->read();

// Print name of element
echo "The name of element is: "
     . "$XMLReader->name<br>";
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/xmlreader.read.php](https://www.php.net/manual/en/xmlreader.read.php)