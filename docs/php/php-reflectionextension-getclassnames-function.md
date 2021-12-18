# PHP|ReflectionExtension getClassNames()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionextension-getclassnames-function/](https://www.geeksforgeeks.org/php-reflectionextension-getclassnames-function/)

**ReflectionExtension：：getClassNames()函数**是 PHP 中的内置函数，用于返回指定扩展的类名数组。 如果未指定类，则返回空数组。

**语法：**

```php
*array* ReflectionExtension::getClassNames( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定扩展名的类名数组。

下面的程序演示了 PHP 中的 ReflectionExtension：：getClassNames()函数：

**程序 _1：**

```php
<?php

// Defining an extension
$A = 'DOM';

// Using ReflectionExtension() over the 
// specified extension
$extension = new ReflectionExtension($A);

// Calling the getClassNames() function
$B = $extension->getClassNames();

// Getting an array of class name
var_dump($B);
?>
```

**输出：**

```php
array(31) {
  [0]=>
  string(12) "DOMException"
  [1]=>
  string(13) "DOMStringList"
  [2]=>
  string(11) "DOMNameList"
  [3]=>
  string(21) "DOMImplementationList"
  [4]=>
  string(23) "DOMImplementationSource"
  [5]=>
  string(17) "DOMImplementation"
  [6]=>
  string(7) "DOMNode"
  [7]=>
  string(16) "DOMNameSpaceNode"
  [8]=>
  string(19) "DOMDocumentFragment"
  [9]=>
  string(11) "DOMDocument"
  [10]=>
  string(11) "DOMNodeList"
  [11]=>
  string(15) "DOMNamedNodeMap"
  [12]=>
  string(16) "DOMCharacterData"
  [13]=>
  string(7) "DOMAttr"
  [14]=>
  string(10) "DOMElement"
  [15]=>
  string(7) "DOMText"
  [16]=>
  string(10) "DOMComment"
  [17]=>
  string(11) "DOMTypeinfo"
  [18]=>
  string(18) "DOMUserDataHandler"
  [19]=>
  string(11) "DOMDomError"
  [20]=>
  string(15) "DOMErrorHandler"
  [21]=>
  string(10) "DOMLocator"
  [22]=>
  string(16) "DOMConfiguration"
  [23]=>
  string(15) "DOMCdataSection"
  [24]=>
  string(15) "DOMDocumentType"
  [25]=>
  string(11) "DOMNotation"
  [26]=>
  string(9) "DOMEntity"
  [27]=>
  string(18) "DOMEntityReference"
  [28]=>
  string(24) "DOMProcessingInstruction"
  [29]=>
  string(15) "DOMStringExtend"
  [30]=>
  string(8) "DOMXPath"
}

```

**程序 _2：**

```php
<?php

// Using ReflectionExtension() over 
// a extension xml
$extension = new ReflectionExtension('xml');

// Calling the getClassNames() function and
// Getting an array of class names
var_dump($extension->getClassNames());
?>
```

**输出：**

```php
array(0) {
}

```

**引用：**[https://www.php.net/manual/en/reflectionextension.getclassnames.php](https://www.php.net/manual/en/reflectionextension.getclassnames.php)