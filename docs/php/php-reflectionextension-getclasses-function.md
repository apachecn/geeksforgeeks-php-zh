# PHP|ReflectionExtension getClasses()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionextension-getclasses-function/](https://www.geeksforgeeks.org/php-reflectionextension-getclasses-function/)

**ReflectionExtension：：getClasses()函数**是 PHP 中的内置函数，用于返回指定扩展的类列表。 如果未指定类，则返回空数组。

**语法：**

```
*array* ReflectionExtension::getClasses( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定扩展的类列表。

下面的程序演示了 PHP 中的 ReflectionExtension：：getClasses()函数：

**程序 _1：**

```
<?php

// Defining an extension
$A = 'DOM';

// Using ReflectionExtension() over the 
// specified extension
$extension = new ReflectionExtension($A);

// Calling the getClasses() function
$B = $extension->getClasses();

// Getting the list of classes
var_dump($B);
?>
```

**输出：**

```
array(31) {
  ["DOMException"]=>
  object(ReflectionClass)#2 (1) {
    ["name"]=>
    string(12) "DOMException"
  }
  ["DOMStringList"]=>
  object(ReflectionClass)#3 (1) {
    ["name"]=>
    string(13) "DOMStringList"
  }
  ["DOMNameList"]=>
  object(ReflectionClass)#4 (1) {
    ["name"]=>
    string(11) "DOMNameList"
  }
  ["DOMImplementationList"]=>
  object(ReflectionClass)#5 (1) {
    ["name"]=>
    string(21) "DOMImplementationList"
  }
  ["DOMImplementationSource"]=>
  object(ReflectionClass)#6 (1) {
    ["name"]=>
    string(23) "DOMImplementationSource"
  }
  ["DOMImplementation"]=>
  object(ReflectionClass)#7 (1) {
    ["name"]=>
    string(17) "DOMImplementation"
  }
  ["DOMNode"]=>
  object(ReflectionClass)#8 (1) {
    ["name"]=>
    string(7) "DOMNode"
  }
  ["DOMNameSpaceNode"]=>
  object(ReflectionClass)#9 (1) {
    ["name"]=>
    string(16) "DOMNameSpaceNode"
  }
  ["DOMDocumentFragment"]=>
  object(ReflectionClass)#10 (1) {
    ["name"]=>
    string(19) "DOMDocumentFragment"
  }
  ["DOMDocument"]=>
  object(ReflectionClass)#11 (1) {
    ["name"]=>
    string(11) "DOMDocument"
  }
  ["DOMNodeList"]=>
  object(ReflectionClass)#12 (1) {
    ["name"]=>
    string(11) "DOMNodeList"
  }
  ["DOMNamedNodeMap"]=>
  object(ReflectionClass)#13 (1) {
    ["name"]=>
    string(15) "DOMNamedNodeMap"
  }
  ["DOMCharacterData"]=>
  object(ReflectionClass)#14 (1) {
    ["name"]=>
    string(16) "DOMCharacterData"
  }
  ["DOMAttr"]=>
  object(ReflectionClass)#15 (1) {
    ["name"]=>
    string(7) "DOMAttr"
  }
  ["DOMElement"]=>
  object(ReflectionClass)#16 (1) {
    ["name"]=>
    string(10) "DOMElement"
  }
  ["DOMText"]=>
  object(ReflectionClass)#17 (1) {
    ["name"]=>
    string(7) "DOMText"
  }
  ["DOMComment"]=>
  object(ReflectionClass)#18 (1) {
    ["name"]=>
    string(10) "DOMComment"
  }
  ["DOMTypeinfo"]=>
  object(ReflectionClass)#19 (1) {
    ["name"]=>
    string(11) "DOMTypeinfo"
  }
  ["DOMUserDataHandler"]=>
  object(ReflectionClass)#20 (1) {
    ["name"]=>
    string(18) "DOMUserDataHandler"
  }
  ["DOMDomError"]=>
  object(ReflectionClass)#21 (1) {
    ["name"]=>
    string(11) "DOMDomError"
  }
  ["DOMErrorHandler"]=>
  object(ReflectionClass)#22 (1) {
    ["name"]=>
    string(15) "DOMErrorHandler"
  }
  ["DOMLocator"]=>
  object(ReflectionClass)#23 (1) {
    ["name"]=>
    string(10) "DOMLocator"
  }
  ["DOMConfiguration"]=>
  object(ReflectionClass)#24 (1) {
    ["name"]=>
    string(16) "DOMConfiguration"
  }
  ["DOMCdataSection"]=>
  object(ReflectionClass)#25 (1) {
    ["name"]=>
    string(15) "DOMCdataSection"
  }
  ["DOMDocumentType"]=>
  object(ReflectionClass)#26 (1) {
    ["name"]=>
    string(15) "DOMDocumentType"
  }
  ["DOMNotation"]=>
  object(ReflectionClass)#27 (1) {
    ["name"]=>
    string(11) "DOMNotation"
  }
  ["DOMEntity"]=>
  object(ReflectionClass)#28 (1) {
    ["name"]=>
    string(9) "DOMEntity"
  }
  ["DOMEntityReference"]=>
  object(ReflectionClass)#29 (1) {
    ["name"]=>
    string(18) "DOMEntityReference"
  }
  ["DOMProcessingInstruction"]=>
  object(ReflectionClass)#30 (1) {
    ["name"]=>
    string(24) "DOMProcessingInstruction"
  }
  ["DOMStringExtend"]=>
  object(ReflectionClass)#31 (1) {
    ["name"]=>
    string(15) "DOMStringExtend"
  }
  ["DOMXPath"]=>
  object(ReflectionClass)#32 (1) {
    ["name"]=>
    string(8) "DOMXPath"
  }
}

```

**程序 _2：**

```
<?php

// Using ReflectionExtension() over 
// a extension xml
$extension = new ReflectionExtension('xml');

// Calling the getClasses() function and
// Getting the list of classes
var_dump($extension->getClasses());
?>
```

**输出：**

```
array(0) {
}

```

**引用：**[https://www.php.net/manual/en/reflectionextension.getclasses.php](https://www.php.net/manual/en/reflectionextension.getclasses.php)