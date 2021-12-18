# PHP|XMLReader getAttribute()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-getattribute-function/](https://www.geeksforgeeks.org/php-xmlreader-getattribute-function/)

**XMLReader：：getAttribute()函数**是 PHP 中的一个内置函数，用于获取命名属性的值。

**语法：**

```
*string* XMLReader::getAttribute( *string* $name )
```

**参数：**此函数接受保存属性名称的单个参数**$name**。

**返回值：**此函数返回属性的值，如果未找到具有给定名称的属性或未位于元素节点上，则返回 NULL。

下面的示例说明 PHP 中的**XMLReader：：getAttribute()函数**：

**示例 1：**

加入时间：清华大学 2007 年 01 月 25 日下午 3：33

```
<?xml version="1.0" encoding="utf-8"?>
<body>
    <h1> Hello </h1>
</body>
```

**index.php**

```
<?php

// Create a new XMLReader instance
$XMLReader = new XMLReader();

// Load the XML file
$XMLReader->open('data.xml');

// Iterate through the XML
while ($XMLReader->read()) {
    if ($XMLReader->nodeType == XMLREADER::ELEMENT) {
        // Get the value of attribute with name id
        $value = $XMLReader->getAttribute('id');

        // Output the value to browser
        echo $value;
    }
}
?>
```

发帖主题：Re：Колибри0.7.0

```
// Empty string because there is no attributes with name id
```

**程序 2：**
**data.xml**

```
<?xml version="1.0" encoding="utf-8"?>
<body>
    <h1 id="geeksforgeeks"> Hello </h1>
    <h2 id="my_id"> World </h2>
</body>
```

**index.php**

```
<?php

// Create a new XMLReader instance
$XMLReader = new XMLReader();

// Load the XML file
$XMLReader->open('data.xml');

// Iterate through the XML
while ($XMLReader->read()) {
    if ($XMLReader->nodeType == XMLREADER::ELEMENT) {

        // Get the value of attribute with name id
        $value = $XMLReader->getAttribute('id');

        // Output the value to browser
        echo $value . "<br>";
    }
}
?>
```

发帖主题：Re：Колибри0.7.0

```
geeksforgeeks
my_id
```

**引用：**[https://www.php.net/manual/en/xmlreader.getattribute.php](https://www.php.net/manual/en/xmlreader.getattribute.php)