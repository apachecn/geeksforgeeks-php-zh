# PHP|XMLReader moveToElement()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-movetoelement-function/](https://www.geeksforgeeks.org/php-xmlreader-movetoelement-function/)

**XMLReader：：moveToElement()函数**是 PHP 中的一个内置函数，用于将光标移动到当前属性的父元素。 通过将此函数与*XMLReader：：moveToAttribute()*函数结合使用，可以使用此函数获取具有特定属性的元素。

**语法：**

```
*bool* XMLReader::moveToElement( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**调用此方法时，如果函数成功，则返回 TRUE；如果失败或未定位在属性上，则返回 FALSE。

下面给出的程序演示了 PHP 中的**XMLReader：：moveToElement()函数**：

**程序 1：**在本程序中，我们将获得属性为*“attrib”*的元素的名称

加入：清华 2007 年 01 月 25 日下午 3：33 发布时间：338

**文件名：***index.php*

```
<?php

// Create a new XMLReader instance
$XMLReader = new XMLReader();

// Open the XML file
$XMLReader->open('data.xml');

// Iterate through the XML nodes
// to reach the h1 node
$XMLReader->read();
$XMLReader->read();
$XMLReader->read();

// Move to attribute with name attrib
$XMLReader->moveToAttribute("attrib");

// Move cursor to the element of attribute
$XMLReader->moveToElement();

// Output the name of element to browser
echo $XMLReader->name;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**在此程序中，我们将获得属性为*“attrib”的所有元素的名称。*

加入：清华 2007 年 01 月 25 日下午 3：33 发布时间：338

**文件名：***index.php*

```
<?php

// Create a new XMLReader instance
$XMLReader = new XMLReader();

// Open the XML file
$XMLReader->open('data.xml');

// Iterate through the XML nodes
while ($XMLReader->read()) {
    if ($XMLReader->nodeType == XMLREADER::ELEMENT) {

        // Get the element name if attribute
        // name is "attrib"
        if ($XMLReader->moveToAttribute("attrib")) {

            // Move cursor to the element of attribute
            $XMLReader->moveToElement();

            // Output the value to browser
            echo $XMLReader->name . "<br>";
        }

    }
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/xmlreader.movetoelement.php](https://www.php.net/manual/en/xmlreader.movetoelement.php)