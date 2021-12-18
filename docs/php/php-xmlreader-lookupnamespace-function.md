# PHP|XMLReader lookupNamespace()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-lookupnamespace-function/](https://www.geeksforgeeks.org/php-xmlreader-lookupnamespace-function/)

**XMLReader：：lookupNamespace()函数**是 PHP 中的一个内置函数，用于在作用域名称空间中查找给定前缀。

**语法：**

```
*string* XMLReader::lookupNamespace( *string* $prefix )
```

**参数：**此函数接受单个参数**$prefix**，该参数保存包含前缀的字符串。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序演示了 PHP 中的**XMLReader：：lookupNamespace()函数**：

加入：清华 2007 年 1 月 25 日下午 3：33 岗位：287 岗位：338 岗位：338 岗位：321загрузкаиспользованияпрограмметсяпрограмметсяпрограмма

```
<?xml version="1.0" encoding="utf-8"?>
<div xmlns:z="my_namespace">
    <z:h1 z:attrib="value"> Foo Bar </z:h1>
</div>
```

**文件名：***index.php*

```
<?php

// Create a new XMLReader instance
$XMLReader = new XMLReader();

// Open the XML file
$XMLReader->open('data.xml');

// Read the node
$XMLReader->read();

// Get the namespace with prefix y
$NS = $XMLReader->lookupNamespace("y");

// Show the namespace to browser
echo $NS;
?>
```

发帖主题：Re：Колибри0.7.0

```
// Empty string because there is no namespace with prefix y.
```

加入：清华 2007 年 1 月 25 日下午 3：33 岗位：287 岗位：338 岗位：338 岗位：321загрузкаиспользованияпрограмметсяпрограмметсяпрограмма

```
<?xml version="1.0" encoding="utf-8"?>
<div xmlns:x="geeksforgeeks">
    <x:h1 x:attrib="value"> Namespaced Text </x:h1>
</div>
```

**文件名：***index.php*

```
<?php

// Create a new XMLReader instance
$XMLReader = new XMLReader();

// Open the XML file
$XMLReader->open('data.xml');

// Read the node
$XMLReader->read();

// Get the namespace with prefix x
$NS = $XMLReader->lookupNamespace("x");

// Show the namespace to browser
echo $NS;
?>
```

发帖主题：Re：Колибри0.7.0

```
geeksforgeeks
```

**引用：**[https://www.php.net/manual/en/xmlreader.lookupnamespace.php](https://www.php.net/manual/en/xmlreader.lookupnamespace.php)