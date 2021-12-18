# PHP|DOMDocument getElementsByTagnameNS()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-getelementsbytagnamens-function/](https://www.geeksforgeeks.org/php-domdocument-getelementsbytagnamens-function/)

**DOMDocument：：getElementsByTagNameNS()函数**是 PHP 中的内置函数，用于搜索指定名称空间中具有给定标记名的所有元素。

**语法：**

```php
*DOMNodeList* DOMDocument::getElementsByTagNameNS( 
            *string* $namespaceURI, *string* $localName )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$nampaceURI：**它指定要匹配的元素的命名空间 URI，*匹配所有命名空间。
*   **$localName：**它指定要匹配的元素的本地名称，*匹配所有本地名称。

**返回值：**此函数返回具有给定本地名称和命名空间 URI 的所有元素的 DOMNodeList。

下面给出的程序演示了 PHP 中的**DOMDocument：：getElementsByTagNameNS()函数**：

**程序 1：**在本例中，我们将获取具有特定命名空间的元素的本地名称和前缀。

## PHP

```php
<?php
// Create an XML
$xml = <<<EOD
<?xml version="1.0" ?>
<!-- this is the namespace -->
<chapter xmlns:xi="my_namespace">
<title>Books of the other guy..</title>
<para>
    <xi:include>
        <xi:fallback>
        </xi:fallback>
    </xi:include>
</para>
</chapter>
EOD;

$dom = new DOMDocument;

// Load the XML string defined above
$dom->loadXML($xml);

// Use getElementsByTagName to get
// the elements from xml
foreach ($dom->getElementsByTagNameNS(
        'my_namespace', '*') as $element) {
    echo '<b>Local name:</b> ',
        $element->localName,
        ', <b>Prefix: </b>',
        $element->prefix, "<br>";
}

?>
```

发帖主题：Re：Колибри0.7.0

```php
Local name: include, Prefix: xi
Local name: fallback, Prefix: xi
```

**程序 2：**在本例中，我们将获得某个名称空间的元素数量。

## PHP

```php
<?php
// Create an XML
$xml = <<<EOD
<?xml version="1.0" ?>
<!-- this is the namespace -->
<chapter xmlns:xi="my_namespace">
<title>Books of the other guy..</title>
<para>
    <xi:include>        <!--  1st -->
        <xi:fallback>   <!--  2nd -->
        </xi:fallback>
    </xi:include>
    <xi:include>        <!--  3rd -->
        <xi:fallback>   <!--  4th -->
        </xi:fallback>
    </xi:include>
</para>
</chapter>
EOD;

$dom = new DOMDocument();

// Load the XML string defined above
$dom->loadXML($xml);

// It will count all occurrence of
// xi inside my_namespace
$elements = $dom->getElementsByTagNameNS(
            'my_namespace', '*');

print_r($elements->length);
?>
```

发帖主题：Re：Колибри0.7.0

```php
4
```

**引用：**[https://www.php.net/manual/en/domdocument.getelementsbytagnamens.php](https://www.php.net/manual/en/domdocument.getelementsbytagnamens.php)