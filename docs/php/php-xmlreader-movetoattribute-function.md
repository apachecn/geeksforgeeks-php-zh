# PHP|XMLReader moveToAttribute()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-movetoattribute-function/](https://www.geeksforgeeks.org/php-xmlreader-movetoattribute-function/)

**XMLReader：：moveToAttribute()函数**是 PHP 中的一个内置函数，用于将光标移动到命名属性。

**语法：**

```php
*bool* XMLReader::moveToAttribute( *string* $name )
```

**参数：**此函数接受保存属性名称的单个参数**$name**。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序演示了 PHP 中的**XMLReader：：moveToAttribute()函数**：

加入：清华 2007 年 1 月 25 日下午 3：33 岗位：287 岗位：338 岗位：338 岗位：321загрузкаиспользованияпрограмметсяпрограмметсяпрограмма

```php
<?xml version="1.0" encoding="utf-8"?>
<div>
    <h1> GeeksforGeeks </h1>
</div>
```

**文件名：***index.php*

```php
<?php

// Create a new XMLReader instance
$XMLReader = new XMLReader();

// Open the XML file
$XMLReader->open('data.xml');

// Iterate through the XML nodes
while ($XMLReader->read()) {
    if ($XMLReader->nodeType == XMLREADER::ELEMENT) {

        // Move to attribute of name "class"
        $XMLReader->moveToAttribute("class");

        // Output the value to browser
        echo $XMLReader->value;
    }
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
// Empty string because there is no attribute with given name.
```

加入：清华 2007 年 1 月 25 日下午 3：33 岗位：287 岗位：338 岗位：338 岗位：321загрузкаиспользованияпрограмметсяпрограмметсяпрограмма

```php
<?xml version="1.0" encoding="utf-8"?>
<div>
    <h1 attrib="value"> My Text </h1>
</div>
```

**文件名：***index.php*

```php
<?php
// Create a new XMLReader instance
$XMLReader = new XMLReader();

// Open the XML file
$XMLReader->open('data.xml');

// Iterate through the XML nodes
while ($XMLReader->read()) {
    if ($XMLReader->nodeType == XMLREADER::ELEMENT) {

        // Move to attribute of name "attrib"
        $XMLReader->moveToAttribute("attrib");

        // Output the value to browser
        echo $XMLReader->value;
    }
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
value
```

**引用：**[https://www.php.net/manual/en/xmlreader.movetoattribute.php](https://www.php.net/manual/en/xmlreader.movetoattribute.php)