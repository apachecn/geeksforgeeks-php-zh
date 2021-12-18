# PHP|XMLReader moveToAttributeNo()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-movetoattributeno-function/](https://www.geeksforgeeks.org/php-xmlreader-movetoattributeno-function/)

**XMLReader：：moveToAttributeNo()函数**是 PHP 中的一个内置函数，用于按索引将光标移动到属性。 当节点具有多个属性，但我们只需要特定属性时，此函数非常有用。

**语法：**

```php
*bool* XMLReader::moveToAttributeNo( *int* $index )
```

**参数：**此函数接受保存属性位置的单个参数**$index**。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序演示了 PHP 中的**XMLReader：：moveToAttributeNo()函数**：

**程序 1：**在此程序中，我们将获取特定节点的第二个属性的值。

加入：清华 2007 年 01 月 25 日下午 3：33 发布时间：338

**文件名：***index.php*

```php
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

// Move to second attribute
// of current node
$XMLReader->moveToAttributeNo(1);

// Output the value to browser
echo $XMLReader->value;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**在此程序中，我们将获取所有节点的第一个属性的值。

加入：清华 2007 年 01 月 25 日下午 3：33 发布时间：338

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

        // Move to first attribute
        $XMLReader->moveToAttributeNo(0);

        // Output the value to browser
        echo $XMLReader->value;
    }
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/xmlreader.movetoattributeno.php](https://www.php.net/manual/en/xmlreader.movetoattributeno.php)