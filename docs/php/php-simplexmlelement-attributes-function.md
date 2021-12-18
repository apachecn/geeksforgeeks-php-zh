# PHP|SimpleXMLElement Attributes()函数

> Original: [https://www.geeksforgeeks.org/php-simplexmlelement-attributes-function/](https://www.geeksforgeeks.org/php-simplexmlelement-attributes-function/)

**先决条件：**[读取 XML 基础知识](https://www.geeksforgeeks.org/xml-basics/)
SimpleXMLElement：：Attributes()函数是 PHP 中的内置函数，用于从 SimpleXML 对象的 XML 标记检索属性及其值。

**语法：**

```
*SimpleXMLElement* SimpleXMLElement::attributes( $namespace, $is_prefix )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$NAMESPACE：**可选参数。 它指定检索到的属性的命名空间。
*   **$is_prefix：**它是布尔参数。 如果$NAMESPACE 是前缀，则为 True；如果$NAMESPACE 为 URI，则为 False。 其默认值为 False。

**返回值：**它返回一个 SimpleXMLElement 对象，该对象可以在 SimpleXMLElement 对象的标记的属性上迭代。 如果 SimpleXMLElement 对象已经是属性而不是标记，则返回 NULL。
**注意：**此函数在 PHP 5.0.1 和更新版本中可用。
下面的程序说明 PHP：
**程序 1：**中的 SimpleXMLElement：：Attributes()函数

## PHP

```
<?php

// Loading XML document to $user
$user = <<<XML
<user>
    <username>
        Geeks123
    </username>

    <name>
        GeeksforGeeks
    </name>

    <phone>
        +91-XXXXXXXXXX
    </phone>

    <address font-color="blue" font="awesome-fonts"
            font-size="24px">
        Noida, UP, India
    </address>
</user>
XML;

// Loading string as simple xml object
$xml = simplexml_load_string($user);

// Print children attribute with its value
foreach($xml->address[0]->attributes() as $key => $value)
{
    echo $key . " => " . $value . "</br>";
}

?>
```