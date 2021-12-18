# PHP|XMLReader isValid()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-isvalid-function/](https://www.geeksforgeeks.org/php-xmlreader-isvalid-function/)

**XMLReader：：isValid()函数**是 PHP 中的一个内置函数，用于检查正在解析的文档是否有效。 如果 XML 是按照 DTD(文档类型定义)编写的，DTD(文档类型定义)定义了所有允许的元素和元素的结构，则 XML 是有效的。

**语法：**

```php
*bool* XMLReader::isValid( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序演示了 PHP 中的**XMLReader：：isValid()函数**：

加入：清华 2007 年 1 月 25 日下午 3：33 岗位：287 岗位：338 岗位：338 岗位：321загрузкаиспользованияпрограмметсяпрограмметсяпрограмма

```php
<?xml version="1.0"?>
<!-- DTD rules to be followed by XML-->
<!DOCTYPE html [
<!ELEMENT html (h1, p, heading, body)>
<!ELEMENT h1 (#PCDATA)>
<!ELEMENT p (#PCDATA)>
<!ELEMENT heading (#PCDATA)>
<!ELEMENT body (#PCDATA)>
]>

<!-- XML starts from here -->
<html>
<h1>Hi</h1>
<p>World</p>
<heading>GeeksforGeeks</heading>
<body>Web Portal for Geeks</body>
</html>
```

**文件名：***index.php*

```php
<?php

// Create a new XMLReader instance
$XMLReader = new XMLReader();

// Open the XML file
$XMLReader->open('data.xml');

// Enable the Parser Property
$XMLReader->setParserProperty(
       XMLReader::VALIDATE, true);

// Iterate through the XML nodes
while ($XMLReader->read()) {
    if ($XMLReader->nodeType == XMLREADER::ELEMENT) {

        // Check if XML is valid or not
        $isValid = $XMLReader->isValid();
        if ($isValid) {
            echo "YES ! this node is validated<br>";
        }
    }
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
YES ! this node is validated
YES ! this node is validated
YES ! this node is validated
YES ! this node is validated
YES ! this node is validated
```

加入：清华 2007 年 1 月 25 日下午 3：33 岗位：287 岗位：338 岗位：338 岗位：321загрузкаиспользованияпрограмметсяпрограмметсяпрограмма

```php
<?xml version="1.0"?>
<!-- DTD rules to be followed by XML-->
<!DOCTYPE html [
<!ELEMENT html (heading, body)>
<!ELEMENT heading (#PCDATA)>
<!ELEMENT body (#PCDATA)>
]>
<!-- XML starts from here -->
<html>
<body>Web Portal for Geeks</body>
</html>
```

**文件名：***index.php*

```php
<?php

// Create a new XMLReader instance
$XMLReader = new XMLReader();

// Open the XML file
$XMLReader->open('data.xml');

// Enable the Parser Property
$XMLReader->setParserProperty(
         XMLReader::VALIDATE, true);

// Iterate through the XML nodes
while ($XMLReader->read()) {
    if ($XMLReader->nodeType == XMLREADER::ELEMENT) {

        // Check if XML is valid or not
        $isValid = $XMLReader->isValid();
        if (!$isValid) {
            echo "No ! this node is not validated<br>";
        }
    }
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
No ! this node is not validated
No ! this node is not validated
```

**引用：**[https://www.php.net/manual/en/xmlreader.isvalid.php](https://www.php.net/manual/en/xmlreader.isvalid.php)