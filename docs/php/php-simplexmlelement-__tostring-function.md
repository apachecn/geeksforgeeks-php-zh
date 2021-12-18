# PHP|SimpleXMLElement__toString()函数

> Original: [https://www.geeksforgeeks.org/php-simplexmlelement-__tostring-function/](https://www.geeksforgeeks.org/php-simplexmlelement-__tostring-function/)

**XMLReader：：__toString()函数**是 PHP 中的一个内置函数，用于获取直接位于当前元素中的文本内容。 此函数不返回此元素的子级中的文本内容。

**语法：**

```php
*void* XMLReader::__toString( *void* )
```

**参数：**此函数不接受任何参数。
**返回值：**此函数成功时返回字符串内容，失败时返回空字符串。

下面的示例说明了 PHP 中的**XMLReader：：__toString()函数**：

**示例 1：**

## PHP

```php
<?php

// Create the XML
$xmlstr = <<<XML
<?xml version='1.0'?>
<library>
  GeeksforGeeks
</library>
XML;

// Create a new SimpleXMLElement
$SXE = new SimpleXMLElement($xmlstr);

// Get the content
$string = $SXE->__toString();
echo $string;
?>
```

发帖主题：Re：Колибри0.7.0

```php
GeeksforGeeks
```

**示例 2：**

## PHP

```php
<?php

// Create the XML
$xmlstr = <<<XML
<?xml version='1.0'?>
<div>
  <sub>
  This text should not be visible
  </sub>
</div>
XML;

// Create a new SimpleXMLElement
$SXE = new SimpleXMLElement($xmlstr);

// Add the attribute
$string = $SXE->__toString();
echo $string;
?>
```

发帖主题：Re：Колибри0.7.0

```php
// Empty string because text content is in a children node not current node.
```

**引用：**[https://www.php.net/manual/en/simplexmlelement.tostring.php](https://www.php.net/manual/en/simplexmlelement.tostring.php)