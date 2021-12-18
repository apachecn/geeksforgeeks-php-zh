# PHP|XMLReader Next()函数

> Original: [https://www.geeksforgeeks.org/php-xmlreader-next-function/](https://www.geeksforgeeks.org/php-xmlreader-next-function/)

**XMLReader：：Next()函数**是 PHP 中的一个内置函数，用于将光标移动到下一个节点，跳过所有子树。 此函数的另一个用法是，它接受节点的名称以直接移动到元素。

**语法：**

```
*bool* XMLReader::next( *string* $localname )
```

**参数：**此函数接受单个参数**$localname**，该参数保存要移动的下一个节点的名称。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的**XMLReader：：Next()函数**：

**程序 1：**在本程序中，我们将遍历 XML 树。
**文件名：***data.xml*

```
<?xml version="1.0" encoding="utf-8"?>
<div1>
    <h1> Foo Bar </h1>
    <div2>
        <h1> Foo Bar </h1>
    </div2>
</div1>
```

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
$XMLReader->next();

// Print name of element
echo "Before:<br> We are currently"
   . " at: $XMLReader->name<br>";

// Move to next node which is
// text "Foo Bar"
$XMLReader->next();

// Move to next element
// which is div2
$XMLReader->next();

// Print name of element
echo "After:<br> We are currently"
    . " at: $XMLReader->name";
?>
```

**输出：**
**之前：**

```
We are currently at: h1
```

**之后：**

```
We are currently at: div2
```

**程序 2：**在本程序中，我们将转到 XML 树中的特定节点。

加入时间：清华大学 2007 年 01 月 25 日下午 3：33

```
<?xml version="1.0" encoding="utf-8"?>
<div1>
    <h1> Foo Bar </h1>
    <div2>
        <h1> Foo Bar </h1>
    </div2>
    <div3> Hello </div3>
</div1>
```

**文件名：***index.php*

```
<?php

// Create a new XMLReader instance
$XMLReader = new XMLReader();

// Open the XML file
$XMLReader->open('data.xml');

// Iterate through the XML nodes to
// reach the subtrees of div1
$XMLReader->read();
$XMLReader->read();
$XMLReader->next("div2");

// Print name of element
echo "Before:<br> We are currently"
      . "at: $XMLReader->name<br>";

// Move to next node which is
// text "Foo Bar"
$XMLReader->next();

// Move to next element which is div2
$XMLReader->next();

// Print name of element
echo "After:<br> We are currently"
    . " at: $XMLReader->name";
?>
```

**输出：**
**之前：**

```
We are currently at: div2
```

**之后：**

```
We are currently at: div3
```

**引用：**[https://www.php.net/manual/en/xmlreader.next.php](https://www.php.net/manual/en/xmlreader.next.php)