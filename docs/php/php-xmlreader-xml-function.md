# PHP|XMLReader XML()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-xml-function/](https://www.geeksforgeeks.org/php-xmlreader-xml-function/)

**XMLReader：：xml()函数**是 PHP 中的一个内置函数，用于设置包含要解析的 XML 的数据。 Xml()函数与 open 函数的用途相同，但唯一的区别是前者接受 XML 作为字符串，而后者接受它作为单独的**.xml**文件。

**语法：**

```php
*bool* XMLReader::XML( *string* $source, 
*string* $encoding, *int* $options )
```

**参数：**此函数接受三个参数，如上所述，如下所述：

*   **$source:** it specifies the string containing the XML to be parsed.
*   **$ENCODING (optional):** specifies the document encoding or NULL.
*   **$options (optional):** it specifies an optional bit mask.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

**异常：**此函数在静态调用时引发 E_STRICT 错误。

下面的示例说明了 PHP 中的**XMLReader：：XML()函数**：

**示例 1：**

```php
<?php

// Create a new XMLReader instance
$XMLReader = new XMLReader();

$XML = "<?xml version=\"1.0\"?>
<div>
    <p> GeeksforGeeks </p>
</div>";

// Open the XML file
$XMLReader->XML($XML);

// Iterate through the XML nodes
while ($XMLReader->read()) {
    if ($XMLReader->nodeType == XMLREADER::ELEMENT) {

        echo "We are at " . $XMLReader->name . "<br>";

    }
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```php
<?php

// Create a new XMLReader instance
$XMLReader = new XMLReader();

$XML = "<?xml version=\"1.0\"?>
<div>
    <p> GeeksforGeeks </p>
</div>";

// Open the XML file
$XMLReader->XML($XML);

// Read the nodes
$XMLReader->read();

// Read it as a string
$string = $XMLReader->readString();

// Output the string to the browser
echo $string;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/xmlreader.xml.php](https://www.php.net/manual/en/xmlreader.xml.php)