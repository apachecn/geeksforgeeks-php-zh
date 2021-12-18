# 如何在 PHP 中把数组转换成 SimpleXML

> 原文:[https://www . geesforgeks . org/how-convert-array-to-SimpleXML-in-PHP/](https://www.geeksforgeeks.org/how-to-convert-array-to-simplexml-in-php/)

很多时候需要将数据以 XML 格式存储到数据库或文件中以备后用。为了满足这一要求，需要将数据转换为 XML 并保存 XML 文件。

SimpleXML 扩展函数提供了将 XML 转换为对象的工具集。这些对象处理普通的属性选择器和数组迭代器。

**例 1:**

```
<?php
// Code to convert php array to xml document

// Define a function that converts array to xml.
function arrayToXml($array, $rootElement = null, $xml = null) {
    $_xml = $xml;

    // If there is no Root Element then insert root
    if ($_xml === null) {
        $_xml = new SimpleXMLElement($rootElement !== null ? $rootElement : '<root/>');
    }

    // Visit all key value pair
    foreach ($array as $k => $v) {

        // If there is nested array then
        if (is_array($v)) { 

            // Call function for nested array
            arrayToXml($v, $k, $_xml->addChild($k));
            }

        else {

            // Simply add child element. 
            $_xml->addChild($k, $v);
        }
    }

    return $_xml->asXML();
}

// Creating an array for demo
$my_array = array (
'name' => 'GFG',
'subject' => 'CS',

    // Creating nested array.
    'contact_info' => array (
    'city' => 'Noida',
    'state' => 'UP',
    'email' => 'feedback@geeksforgeeks.org'
    ),
);

// Calling arrayToxml Function and printing the result
echo arrayToXml($my_array);
?>
```

**输出:**

```
<?xml version="1.0"?>
<root>
    <name> GFG </name>
    <subject> CS </subject>
    <contact_info >
        <city > Noida < /city >
        <state > UP < /state >
        <email > feedback@geeksforgeeks.org </email>
    <contact_info>
<root>

```

上述问题可以用 array_walk_recursive()函数解决。该函数将数组转换为 xml 文档，其中数组的键被转换为值，数组的值被转换为 xml 元素。

**例 2:**

```
<?php
// Code to convert php array to xml document

// Creating an array
$my_array = array (
    'a' => 'x',
    'b' => 'y',

    // creating nested array
    'another_array' => array (
        'c' => 'z',
    ),
);

// This function create a xml object with element root.
$xml = new SimpleXMLElement('<root/>');

// This function resursively added element
// of array to xml document
array_walk_recursive($my_array, array ($xml, 'addChild'));

// This function prints xml document.
print $xml->asXML();
?>
```

**输出:**

```
<?xml version="1.0"? >
<root >
       <x> a </x >
       <y> b </y >
       <z> c </z >
</root >

```

**注意:**如果系统产生错误类型:PHP 致命错误:未捕获错误:在/home/6b c 5567266 b 35 AE 3e 76d 84307 E5 BDC 78 . PHP:24 中找不到类“SimpleXMLElement”，那么只需安装 *php-xml、php-simplexml* 包即可。