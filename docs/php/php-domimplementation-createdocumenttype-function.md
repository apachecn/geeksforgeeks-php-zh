# PHP|DOMImplementation createDocumentType()函数

> Original: [https://www.geeksforgeeks.org/php-domimplementation-createdocumenttype-function/](https://www.geeksforgeeks.org/php-domimplementation-createdocumenttype-function/)

**DOMImplementation：：createDocumentType()函数**是 PHP 中的内置函数，用于创建空的 DOMDocumentType 对象。 实体声明和符号不可用。

**语法：**

```
*DOMDocumentType* DOMImplementation::createDocumentType
( *string* $qualifiedName = NULL, *string* $publicId = NULL,
 *string* $systemId = NULL )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$QualifiedName(可选)：**它指定要创建的文档类型的限定名称。
*   **$public Id(可选)：**它指定外部子集公共标识符的限定名称。
*   **$systemId(可选)：**它指定外部子集系统标识符。

**返回值：**此函数返回 ownerDocument 设置为空的 DOMDocumentType 节点。

**异常：**如果命名空间有错误，则此函数抛出*DOM_NAMESPACE_ERR*，由**$QualifiedName**确定。

下面给出的程序说明了 PHP：
**程序 1：**中的**DOMImplementation：：createDocumentType()函数**

```
<?php

// Creates an instance of the DOMImplementation class
$imp = new DOMImplementation();

// Creates a DOMDocumentType instance
$dtd = $imp->createDocumentType(
'svg:svg', null, 'http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd');

// Get the systemId
echo $dtd->systemId;
?>
```

发帖主题：Re：Колибри0.7.0

```
http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd
```

**程序 2：**

```
<?php
// Creates an instance of the DOMImplementation class
$imp = new DOMImplementation();

// Creates a DOMDocumentType instance
$dtd = $imp->createDocumentType('GeeksforGeeks');

// Get the name
echo $dtd->name;
?>
```

发帖主题：Re：Колибри0.7.0

```
GeeksforGeeks
```

**引用：**[https://www.php.net/manual/en/domimplementation.createdocumenttype.php](https://www.php.net/manual/en/domimplementation.createdocumenttype.php)