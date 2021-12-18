# PHP|SimpleXMLElement registerXPathNamespace()函数

> Original: [https://www.geeksforgeeks.org/php-simplexmlelement-registerxpathnamespace-function/](https://www.geeksforgeeks.org/php-simplexmlelement-registerxpathnamespace-function/)

**先决条件：**[阅读 XML 基础知识](https://www.geeksforgeeks.org/xml-basics/)

SimpleXMLElement：：registerXPathNamespace()函数是 PHP 中的一个内置函数，用于为接下来在 SimpleXML 对象中执行的 XPath 查询创建名称空间上下文。

**语法：**

```
*bool* SimpleXMLElement::registerXPathNamespace( $prefix, $namespace )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$PREFIX：**必选参数。 它在$NAMESPACE 中给定的命名空间的 XPath 查询中使用。
*   **$NAMESPACE：**：它是必需的参数。 它指定 XPath 查询的名称空间。

**返回值：**成功返回 True，失败返回 False。

**注意：**此函数在 PHP 5.2.0 及更新版本中可用。

下面的程序演示了 PHP 中的 SimpleXMLElement：：registerXPathNamespace()函数：

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

// Registering Xpath namespace
$xml->registerXPathNamespace('u', 'http://geeksforgeeks.org/user');

// Retrieving xpaths
$result = $xml->xpath('//u:id');

// Printing output
foreach ($result as $id) {
    echo $id . "<br>";
}

?>
```

**Output:**

```
12345
15980

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

// Registering xpath namespace
$xml->registerXPathNamespace('u', 'http://geeksforgeeks.org/user');
$xml->registerXPathNamespace('un', 'http://geeksforgeeks.org/user/name');

// Retrieving xpaths
$result = $xml->xpath('//u:id');
$result_f_name = $xml->xpath('//un:firstname');
$result_l_name = $xml->xpath('//un:lastname');

// Displaying output
foreach ($result as $id) {
    echo $id . "<br>";
}
foreach ($result_f_name as $f_name) {
    echo $f_name . "<br>";
}
foreach ($result_l_name as $l_name) {
    echo $l_name . "<br>";
}

?>
```

**Output:**

```
12345
57833
98944
Rakesh
Manjeet
Ak
Kumar
Singh
Singh

```

**引用：**[https://www.php.net/manual/en/simplexmlelement.registerxpathnamespace.php](https://www.php.net/manual/en/simplexmlelement.registerxpathnamespace.php)