# PHP|SimpleXMLElement getNamespaces()函数

> Original: [https://www.geeksforgeeks.org/php-simplexmlelement-getnamespaces-function/](https://www.geeksforgeeks.org/php-simplexmlelement-getnamespaces-function/)

**先决条件：**[阅读 XML 基础知识](https://www.geeksforgeeks.org/xml-basics/)

SimpleXMLElement：：getNamespaces()函数是 PHP 中的一个内置函数，用于检索 XML 文档中声明的名称空间。

**语法：**

```
*array* SimpleXMLElement::getNamespaces( $recursive )
```

**参数：**此函数接受可选的单个参数**$recursive**。 其默认值为 False。 如果传递 True，则它递归地返回父节点和子节点中的命名空间。 如果设置为 False，则它只返回父节点的名称空间。

**返回值：**此函数返回名称空间名称及其关联 URI 的数组。

**注意：**此函数适用于 PHP 5.1.2 及更高版本。

下面的程序演示了 PHP 中的 SimpleXMLElement：：getNamespaces()函数：

**程序 1：**

```
<?php

// Loading XML document to $user
$user = <<<XML
<user xmlns:user_id="http://geeksforgeeks.org/user">
<single_user id="1">
    <user_id:id>12345</user_id:id>
    <username>Geeks123</username>
    <name>GeeksforGeeks</name>
    <phone>+91-XXXXXXXXXX</phone>
    <detail font-color="blue" font-size="24px">
        Noida India
    </detail>
</single_user>

<single_user id="2">
    <user_id:id>15980</user_id:id>
    <username>Geeks54321</username>
    <name>Geeks</name>
    <phone>+91-XXXXXXXXXX</phone>
    <detail font-color="blue" font-size="24px">
        Noida India
    </detail>
</single_user>
</user>
XML;

// Loading string as simple xml object
$xml = simplexml_load_string($user);

// Retrieving namespaces
$result = $xml->getNamespaces(1);

// Display output
print_r($result);

?>
```

**输出：**

```
Array
(
    [user_id] => http://geeksforgeeks.org/user
)

```

**程序 2：**

```
<?php

// Loading XML document to $user
$user = <<<XML
<user xmlns:user_id="http://geeksforgeeks.org/user">
    <single_user id="1" xmlns:name="http://geeksforgeeks.org/user/name">
        <user_id:id>12345</user_id:id>
        <username>rakesh123</username>
        <name:firstname>Rakesh</name:firstname>
        <name:lastname>Kumar</name:lastname>
        <phone>+91-XXXXXXXXXX</phone>
        <detail>Noida India</detail>
    </single_user>

    <single_user id="2" xmlns:name="http://geeksforgeeks.org/user/name">
        <user_id:id>57833</user_id:id>
        <username>man123</username>
        <name:firstname>Manjeet</name:firstname>
        <name:lastname>Singh</name:lastname>
        <phone>+91-XXXXXXXXXX</phone>
        <detail>Kolkata, India</detail>
    </single_user>

    <single_user id="3" xmlns:name="http://geeksforgeeks.org/user/name">
        <user_id:id>98944</user_id:id>
        <username>ak98</username>
        <name:firstname>Ak</name:firstname>
        <name:lastname>Singh</name:lastname>
        <phone>+91-XXXXXXXXXX</phone>
        <detail>Noida India</detail>
    </single_user>
</user>
XML;

// Loading string as simple xml object
$xml = simplexml_load_string($user);

// Retrieving namespaces
$result = $xml->getNamespaces(TRUE);

// Displaying output
print_r($result);

?>
```

**输出：**

```
Array
(
    [user_id] => http://geeksforgeeks.org/user
    [name] => http://geeksforgeeks.org/user/name
)

```

**引用：**[https://www.php.net/manual/en/simplexmlelement.getnamespaces.php](https://www.php.net/manual/en/simplexmlelement.getnamespaces.php)