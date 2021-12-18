# PHP|simplexml_load_string()函数

> Original: [https://www.geeksforgeeks.org/php-simplexml_load_string-function/](https://www.geeksforgeeks.org/php-simplexml_load_string-function/)

有时需要在 PHP 中解析 XML 数据。 有几种方法可用于解析 XML 数据。 SimpleXML 就是其中之一。 解析 XML 文档意味着在 XML 文档中导航并返回相关信息。 目前，少数 API 以 JSON 格式返回数据，但仍有大量网站以 XML 格式返回数据。 因此，如果我们想要尽情享受可用的 API，就必须掌握解析 XML 文档的技巧。

PHP SimpleXML 是在 PHP5.0 中引入的。 PHP 中的 simplexml_load_string()函数用于将 XML 字符串解释为对象。

**语法**：

```php
simplexml_load_string($data, $classname, $options, $ns, $is_prefix);

```

**参数**：此函数接受五个参数，如上面的语法所示。 所有这些参数如下所述：

*   **$data**：格式良好的 XML 字符串。
*   **$classname**：新对象的类。
*   **$Options**：通过指定选项和 1 或 0 来设置附加的 Libxml 参数。
*   **$ns**：如果 ns 是前缀，则为 True。 如果 ns 是 URI，则为 False。 默认值为 False
*   **$is_prefix**：如果 ns 是前缀，则为 True。 如果 ns 是 URI，则为 False。 默认值为 False

参数**$Options**的可能值如下：

*   **LIBXML_COMPACT：**激活节点分配优化。
*   加入时间：清华大学 2007 年 01 月 25 日下午 3：33
*   **LIBXML_DTDLOAD：**加载外部子集
*   **LIBXML_DTDVALID：**使用 DTD 进行验证
*   **LIBXML_NOBLANKS：**删除空白节点
*   **LIBXML_NOCDATA：**将 CDATA 合并为文本节点
*   **LIBXML_NOEMPTYTAG：**展开空标记
*   **LIBXML_NOENT：**替换实体
*   **LIBXML_NOERROR：**不显示错误报告<
*   **LIBXML_NONOET：**加载文档时禁用网络访问
*   **LIBXML_NOWARNING：**不显示警告报告
*   **LIBXML_NOXMLDECL：**保存文档时删除 XML 声明
*   **LIBXML_NSCLEAN：**删除多余的命名空间声明
*   **LIBXML_PARSEHUGE：**设置 XML_PARSE_GUGH 标志
*   **LIBXML_XINCLUDE：**实现 XInclude 替换
*   **LIBXML_ERR_ERROR：**获取可恢复的错误
*   **LIBXML_ERR_FATAL：**获取致命错误
*   加入时间：清华大学 2007 年 01 月 25 日下午 3：33
*   **LIBXML_ERR_WARNING：**获取简单警告
*   **LIBXML_VERSION：**获取 libxml 版本
*   **LIBXML_DOTTED_VERSION：**获取以点分隔的 libxml 版本

**返回值**此函数成功时返回 SimpleXMLElement 对象，失败时返回 False。

以下程序说明了 simplexml_load_string()函数：

**程序 1**：

```php
<?php
$note=<<<XML
<note>
  <to>User 1</to>
  <from>User 2</from>
  <heading>Reminder</heading>
  <body>Don't forget me this weekend!</body>
</note>
XML;

$xml = simplexml_load_string($note);
echo $xml->to . "<br>";
echo $xml->from . "<br>";
echo $xml->heading . "<br>";
echo $xml->body;
?>
```

产出：

```php
User 1
User 2
Reminder
Don't forget me this weekend!

```

**程序 2**：

```php
<?php
$note=<<<XML
<?xml version="1.0" encoding="ISO-8859-1"?>
<book>
    <name>PHP</name>
    <name>Java</name>
    <name>C++</name>
    <name>Python</name>
</book>
XML;

$xml=simplexml_load_string($note);
echo $xml->getName() . "\n";

foreach($xml->children() as $child){
   echo $child->getName() . ": " . $child . "\n";
}
?>
```

产出：

```php
book
name : PHP
name : Java
name : C++
name : Python

```

**引用：**
[http://php.net/manual/en/function.simplexml-load-string.php](http://php.net/manual/en/function.simplexml-load-string.php)