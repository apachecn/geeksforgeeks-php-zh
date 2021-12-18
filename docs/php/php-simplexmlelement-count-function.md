# PHP|SimpleXMLElement count()函数

> Original: [https://www.geeksforgeeks.org/php-simplexmlelement-count-function/](https://www.geeksforgeeks.org/php-simplexmlelement-count-function/)

**先决条件：**[阅读 XML 基础知识](https://www.geeksforgeeks.org/xml-basics/)

SimpleXMLElement：：count()函数是 PHP 中内置函数，用于计算 SimpleXML 对象中的子元素数量。

**语法：**

```
*int* SimpleXMLElement::count()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回元素的子级数。

**注意：**此函数适用于 PHP 5.3.0 及更高版本。

**示例 1：**

```
<?php

// Loading XML document to $user
$user = <<<XML
<user>
<username> user123 </username>
<name> firstname lastname </name>
<phone> +91-9876543210 </phone>
<detail> I am John Doe. Live in Kolkata, India. </detail>
</user>
XML;

// Creating new SimpleXMLElement 
// object from $user
$xml = new SimpleXMLElement($user);

// Counting and printing number of
// child of the XML document
echo $xml->count();

?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**对 XML 文档的子元素的子元素进行计数。

```
<?php

// Loading XML document to $user
$user = <<<XML
<users>
    <user name="user1">
        <username> user123 </username>
        <name> firstname lastname </name>
        <phone> +91-9876543210 </phone>
        <detail> I am John Doe. Live in Kolkata, India. </detail>
        <ins>
            <ins_name>geeks for geeks</ins_name>
            <ins_type>educational</ins_type>
            <ins_url>geeksforgeeks.org</ins_url>
        </ins>
    </user>
    <user name="user2">
        <username> user123 </username>
        <name> firstname lastname </name>
        <phone> +91-9876543210 </phone>
        <detail> I am John Doe. Live in Kolkata, India. </detail>
        <ins>
            <ins_name>geeks for geeks</ins_name>
            <ins_type>educational</ins_type>
            <ins_url>geeksforgeeks.org</ins_url>
        </ins>
    </user>    
</users>
XML;

// Creating new SimpleXMLElement
// object from $user
$xml = new SimpleXMLElement($user);

echo $xml->count();

foreach($xml as $child){
    echo "<br>".$child['name'] . " has " 
        . $child->count()." child.";
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/simplexmlelement.count.php](https://www.php.net/manual/en/simplexmlelement.count.php)