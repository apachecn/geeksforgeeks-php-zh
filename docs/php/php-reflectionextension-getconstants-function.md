# PHP|ReflectionExtension getConstants()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionextension-getconstants-function/](https://www.geeksforgeeks.org/php-reflectionextension-getconstants-function/)

**ReflectionExtension：：getConstants()函数**是 PHP 中的内置函数，用于返回常量名称作为键的关联数组。

**语法：**

```php
*array* ReflectionExtension::getConstants( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回以常量名称作为键的关联数组。

下面的程序演示了 PHP 中的 ReflectionExtension：：getConstants()函数：

**程序 1：**

```php
<?php

// Defining an extension
$A = 'DOM';

// Using ReflectionExtension() over the 
// specified extension
$extension = new ReflectionExtension($A);

// Calling the getConstants() function
$B = $extension->getConstants();

// Getting an array with constant names as keys
var_dump($B);
?>
```

**输出：**

```php
array(45) {
  ["XML_ELEMENT_NODE"]=>
  int(1)
  ["XML_ATTRIBUTE_NODE"]=>
  int(2)
  ["XML_TEXT_NODE"]=>
  int(3)
  ["XML_CDATA_SECTION_NODE"]=>
  int(4)
  ["XML_ENTITY_REF_NODE"]=>
  int(5)
  ["XML_ENTITY_NODE"]=>
  int(6)
  ["XML_PI_NODE"]=>
  int(7)
  ["XML_COMMENT_NODE"]=>
  int(8)
  ["XML_DOCUMENT_NODE"]=>
  int(9)
  ["XML_DOCUMENT_TYPE_NODE"]=>
  int(10)
  ["XML_DOCUMENT_FRAG_NODE"]=>
  int(11)
  ["XML_NOTATION_NODE"]=>
  int(12)
  ["XML_HTML_DOCUMENT_NODE"]=>
  int(13)
  ["XML_DTD_NODE"]=>
  int(14)
  ["XML_ELEMENT_DECL_NODE"]=>
  int(15)
  ["XML_ATTRIBUTE_DECL_NODE"]=>
  int(16)
  ["XML_ENTITY_DECL_NODE"]=>
  int(17)
  ["XML_NAMESPACE_DECL_NODE"]=>
  int(18)
  ["XML_LOCAL_NAMESPACE"]=>
  int(18)
  ["XML_ATTRIBUTE_CDATA"]=>
  int(1)
  ["XML_ATTRIBUTE_ID"]=>
  int(2)
  ["XML_ATTRIBUTE_IDREF"]=>
  int(3)
  ["XML_ATTRIBUTE_IDREFS"]=>
  int(4)
  ["XML_ATTRIBUTE_ENTITY"]=>
  int(6)
  ["XML_ATTRIBUTE_NMTOKEN"]=>
  int(7)
  ["XML_ATTRIBUTE_NMTOKENS"]=>
  int(8)
  ["XML_ATTRIBUTE_ENUMERATION"]=>
  int(9)
  ["XML_ATTRIBUTE_NOTATION"]=>
  int(10)
  ["DOM_PHP_ERR"]=>
  int(0)
  ["DOM_INDEX_SIZE_ERR"]=>
  int(1)
  ["DOMSTRING_SIZE_ERR"]=>
  int(2)
  ["DOM_HIERARCHY_REQUEST_ERR"]=>
  int(3)
  ["DOM_WRONG_DOCUMENT_ERR"]=>
  int(4)
  ["DOM_INVALID_CHARACTER_ERR"]=>
  int(5)
  ["DOM_NO_DATA_ALLOWED_ERR"]=>
  int(6)
  ["DOM_NO_MODIFICATION_ALLOWED_ERR"]=>
  int(7)
  ["DOM_NOT_FOUND_ERR"]=>
  int(8)
  ["DOM_NOT_SUPPORTED_ERR"]=>
  int(9)
  ["DOM_INUSE_ATTRIBUTE_ERR"]=>
  int(10)
  ["DOM_INVALID_STATE_ERR"]=>
  int(11)
  ["DOM_SYNTAX_ERR"]=>
  int(12)
  ["DOM_INVALID_MODIFICATION_ERR"]=>
  int(13)
  ["DOM_NAMESPACE_ERR"]=>
  int(14)
  ["DOM_INVALID_ACCESS_ERR"]=>
  int(15)
  ["DOM_VALIDATION_ERR"]=>
  int(16)
}

```

**程序 2：**

```php
<?php

// Using ReflectionExtension() over 
// an extension xml
$extension = new ReflectionExtension('xml');

// Calling the getConstants() function and
// Getting an array with constant names as keys.
var_dump($extension->getConstants());
?>
```

**输出：**

```php
array(27) {
  ["XML_ERROR_NONE"]=>
  int(0)
  ["XML_ERROR_NO_MEMORY"]=>
  int(1)
  ["XML_ERROR_SYNTAX"]=>
  int(2)
  ["XML_ERROR_NO_ELEMENTS"]=>
  int(3)
  ["XML_ERROR_INVALID_TOKEN"]=>
  int(4)
  ["XML_ERROR_UNCLOSED_TOKEN"]=>
  int(5)
  ["XML_ERROR_PARTIAL_CHAR"]=>
  int(6)
  ["XML_ERROR_TAG_MISMATCH"]=>
  int(7)
  ["XML_ERROR_DUPLICATE_ATTRIBUTE"]=>
  int(8)
  ["XML_ERROR_JUNK_AFTER_DOC_ELEMENT"]=>
  int(9)
  ["XML_ERROR_PARAM_ENTITY_REF"]=>
  int(10)
  ["XML_ERROR_UNDEFINED_ENTITY"]=>
  int(11)
  ["XML_ERROR_RECURSIVE_ENTITY_REF"]=>
  int(12)
  ["XML_ERROR_ASYNC_ENTITY"]=>
  int(13)
  ["XML_ERROR_BAD_CHAR_REF"]=>
  int(14)
  ["XML_ERROR_BINARY_ENTITY_REF"]=>
  int(15)
  ["XML_ERROR_ATTRIBUTE_EXTERNAL_ENTITY_REF"]=>
  int(16)
  ["XML_ERROR_MISPLACED_XML_PI"]=>
  int(17)
  ["XML_ERROR_UNKNOWN_ENCODING"]=>
  int(18)
  ["XML_ERROR_INCORRECT_ENCODING"]=>
  int(19)
  ["XML_ERROR_UNCLOSED_CDATA_SECTION"]=>
  int(20)
  ["XML_ERROR_EXTERNAL_ENTITY_HANDLING"]=>
  int(21)
  ["XML_OPTION_CASE_FOLDING"]=>
  int(1)
  ["XML_OPTION_TARGET_ENCODING"]=>
  int(2)
  ["XML_OPTION_SKIP_TAGSTART"]=>
  int(3)
  ["XML_OPTION_SKIP_WHITE"]=>
  int(4)
  ["XML_SAX_IMPL"]=>
  string(6) "libxml"
}

```

**引用：**[https://www.php.net/manual/en/reflectionextension.getconstants.php](https://www.php.net/manual/en/reflectionextension.getconstants.php)