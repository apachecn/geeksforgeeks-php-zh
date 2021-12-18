# PHP|SimpleXMLElement 子代()函数

> Original: [https://www.geeksforgeeks.org/php-simplexmlelement-children-function/](https://www.geeksforgeeks.org/php-simplexmlelement-children-function/)

**先决条件：**[读取 XML 基础知识](https://www.geeksforgeeks.org/xml-basics/)
SimpleXMLElement：：Children()函数是 PHP 中的内置函数，它返回 SimpleXML 对象中给定节点的子节点。

**语法：**

```
*SimpleXMLElement* SimpleXMLElement::children( $namespace, $is_prefix )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$NAMESPACE：**可选参数。 它指定 XML 名称空间。
*   **$is_prefix：**布尔参数，可选。 如果$NAMESPACE 是前缀，则为 True；如果$Namespace 是名称空间 URL，则为 False。 其默认值为 False。

**返回值：**此函数返回 SimpleXMLElement 对象。
**注意：**此函数在 PHP 5.0.1 和更新版本中可用。
下面的程序说明了 PHP：
**程序 1：**中的 SimpleXMLElement：：Child()函数。此程序显示子节点的值。

## PHP

```
<?php

// Loading XML document to $user
$user = <<<XML
<user>
    <username>Geeks123</username>
    <name>GeeksforGeeks</name>
    <phone>+91-XXXXXXXXXX</phone>
    <address>
        Noida, UP, India
    </address>
</user>
XML;

// Loading string as simple xml object
$xml = simplexml_load_string($user);

// Print children node
foreach($xml->children() as $child) {
    echo "Child node: " . $child . "</br>";
}

?>
```