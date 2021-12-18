# PHP|SimpleXMLElement addChild()函数

> Original: [https://www.geeksforgeeks.org/php-simplexmlelement-addchild-function/](https://www.geeksforgeeks.org/php-simplexmlelement-addchild-function/)

**先决条件：**[阅读 XML 基础知识](https://www.geeksforgeeks.org/xml-basics/)

SimpleXMLElement：：addChild()函数是 PHP 中的一个内置函数，用于在 SimpleXML 对象中添加子对象。

**语法：**

```php
*SimpleXMLElement* SimpleXMLElement::addChild($name, $value, $namespace);
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$name：**必选参数。 它指定要添加的子元素的名称。
*   **$value：**可选参数。 它指定要添加的子元素的值。
*   **$NAMESPACE：**可选参数。 它指定子元素的命名空间。

**返回值：**子添加成功时返回 SimpleXMLElement 对象。

**注意：**此函数适用于 PHP 5.1.3 及更高版本。

**示例：**

```php
<?php
// Loading XML document to $user

$user = <<<XML
<user>
<username>user123</username>
<name>firstname lastname</name>
<phone>+91-9876543210</phone>
<detail>I am John Doe. Live in Kolkata, India.</detail>
</user>
XML;

// creating new SimpleXMLElement
// object from $user
$xml = new SimpleXMLElement($user);

// Adding child named "institution"
// and valued "geeksforgeeks"
$xml -> addChild("institution", "geeksforgeeks");

// Printing as XML
echo $xml->asXML();

echo $xml->asXML('savexmltofile.xml');

?>
```

发帖主题：Re：Колибри0.7.0

```php
user123 firstname lastname +91-9876543210 I am John Doe.
Live in Kolkata, India. geeksforgeeks 1

```

**已保存的 XML 文件：**
![](img/cc83fed4ed54e2b9a64a40b3ce7fa16b.png)

**引用：**[https://www.php.net/manual/en/simplexmlelement.addchild.php](https://www.php.net/manual/en/simplexmlelement.addchild.php)