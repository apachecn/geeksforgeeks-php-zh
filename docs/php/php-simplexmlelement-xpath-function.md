# PHP|SimpleXMLElement XPath()函数

> Original: [https://www.geeksforgeeks.org/php-simplexmlelement-xpath-function/](https://www.geeksforgeeks.org/php-simplexmlelement-xpath-function/)

**先决条件：**[阅读 XML 基础知识](https://www.geeksforgeeks.org/xml-basics/)

SimpleXMLElement：：XPath()函数是 PHP 中的一个内置函数，它在 XML 文档上运行 XPath 查询。

**语法：**

```
SimpleXMLElement::xpath( $path )
```

**参数：**此函数接受所需的单个参数**$path**。 用于指定 XML 文档的 XPath 路径。

**返回值：**成功时返回 SimpleXMLElement 数组，失败时返回 False 数组。

**注意：**此函数在 PHP 5.2.0 及更新版本中可用。

**示例：**

```
<?php

// Loading XML document to $user
$user = <<<XML
<user>
    <id>12345</id>
    <username>Geeks123</username>
    <name>GeeksforGeeks</name>
    <phone>+91-XXXXXXXXXX</phone>
    <detail font-color="blue" font-size="24px">
        Noida India
    </detail>
</user>
XML;

// Loading string as simple xml object
$xml = simplexml_load_string($user);

// Retrieving xpaths
$result = $xml->xpath("username");

// Printing output
print_r($result);

?>
```

**Output:**

```
Array
(
    [0] => SimpleXMLElement Object
        (
            [0] => Geeks123
        )

)

```

**示例 2：**

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

// Registering xpath namespace
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

**示例 3：**

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

// Printing output
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

**引用：**[https://www.php.net/manual/en/simplexmlelement.xpath.php](https://www.php.net/manual/en/simplexmlelement.xpath.php)