# PHP|ReflectionExtension getFunctions()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionextension-getfunctions-function/](https://www.geeksforgeeks.org/php-reflectionextension-getfunctions-function/)

**ReflectionExtension：：getFunctions()函数**是 PHP 中的内置函数，用于从指定的扩展返回扩展函数。

**语法：**

```php
*array* ReflectionExtension::getFunctions( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定扩展的扩展函数。

下面的程序演示了 PHP 中的 ReflectionExtension：：getFunctions()函数：

**程序 _1：**

```php
<?php

// Defining an extension
$A = 'DOM';

// Using ReflectionExtension() over the 
// specified extension
$extension = new ReflectionExtension($A);

// Calling the getFunctions() function
$B = $extension->getFunctions();

// Getting extension functions from
// the specified extension.
var_dump($B);
?>
```

**输出：**

```php
array(1) {
  ["dom_import_simplexml"]=>
  object(ReflectionFunction)#2 (1) {
    ["name"]=>
    string(20) "dom_import_simplexml"
  }
}

```

**程序 _2：**

```php
<?php

// Using ReflectionExtension() over 
// a extension xml
$extension = new ReflectionExtension('xml');

// Calling the getFunctions() function and
// Getting extension functions from the
// specified extension.
var_dump($extension->getFunctions());
?>
```

**输出：**

```php
array(24) {
  ["xml_parser_create"]=>
  object(ReflectionFunction)#2 (1) {
    ["name"]=>
    string(17) "xml_parser_create"
  }
  ["xml_parser_create_ns"]=>
  object(ReflectionFunction)#3 (1) {
    ["name"]=>
    string(20) "xml_parser_create_ns"
  }
  ["xml_set_object"]=>
  object(ReflectionFunction)#4 (1) {
    ["name"]=>
    string(14) "xml_set_object"
  }
  ["xml_set_element_handler"]=>
  object(ReflectionFunction)#5 (1) {
    ["name"]=>
    string(23) "xml_set_element_handler"
  }
  ["xml_set_character_data_handler"]=>
  object(ReflectionFunction)#6 (1) {
    ["name"]=>
    string(30) "xml_set_character_data_handler"
  }
  ["xml_set_processing_instruction_handler"]=>
  object(ReflectionFunction)#7 (1) {
    ["name"]=>
    string(38) "xml_set_processing_instruction_handler"
  }
  ["xml_set_default_handler"]=>
  object(ReflectionFunction)#8 (1) {
    ["name"]=>
    string(23) "xml_set_default_handler"
  }
  ["xml_set_unparsed_entity_decl_handler"]=>
  object(ReflectionFunction)#9 (1) {
    ["name"]=>
    string(36) "xml_set_unparsed_entity_decl_handler"
  }
  ["xml_set_notation_decl_handler"]=>
  object(ReflectionFunction)#10 (1) {
    ["name"]=>
    string(29) "xml_set_notation_decl_handler"
  }
  ["xml_set_external_entity_ref_handler"]=>
  object(ReflectionFunction)#11 (1) {
    ["name"]=>
    string(35) "xml_set_external_entity_ref_handler"
  }
  ["xml_set_start_namespace_decl_handler"]=>
  object(ReflectionFunction)#12 (1) {
    ["name"]=>
    string(36) "xml_set_start_namespace_decl_handler"
  }
  ["xml_set_end_namespace_decl_handler"]=>
  object(ReflectionFunction)#13 (1) {
    ["name"]=>
    string(34) "xml_set_end_namespace_decl_handler"
  }
  ["xml_parse"]=>
  object(ReflectionFunction)#14 (1) {
    ["name"]=>
    string(9) "xml_parse"
  }
  ["xml_parse_into_struct"]=>
  object(ReflectionFunction)#15 (1) {
    ["name"]=>
    string(21) "xml_parse_into_struct"
  }
  ["xml_get_error_code"]=>
  object(ReflectionFunction)#16 (1) {
    ["name"]=>
    string(18) "xml_get_error_code"
  }
  ["xml_error_string"]=>
  object(ReflectionFunction)#17 (1) {
    ["name"]=>
    string(16) "xml_error_string"
  }
  ["xml_get_current_line_number"]=>
  object(ReflectionFunction)#18 (1) {
    ["name"]=>
    string(27) "xml_get_current_line_number"
  }
  ["xml_get_current_column_number"]=>
  object(ReflectionFunction)#19 (1) {
    ["name"]=>
    string(29) "xml_get_current_column_number"
  }
  ["xml_get_current_byte_index"]=>
  object(ReflectionFunction)#20 (1) {
    ["name"]=>
    string(26) "xml_get_current_byte_index"
  }
  ["xml_parser_free"]=>
  object(ReflectionFunction)#21 (1) {
    ["name"]=>
    string(15) "xml_parser_free"
  }
  ["xml_parser_set_option"]=>
  object(ReflectionFunction)#22 (1) {
    ["name"]=>
    string(21) "xml_parser_set_option"
  }
  ["xml_parser_get_option"]=>
  object(ReflectionFunction)#23 (1) {
    ["name"]=>
    string(21) "xml_parser_get_option"
  }
  ["utf8_encode"]=>
  object(ReflectionFunction)#24 (1) {
    ["name"]=>
    string(11) "utf8_encode"
  }
  ["utf8_decode"]=>
  object(ReflectionFunction)#25 (1) {
    ["name"]=>
    string(11) "utf8_decode"
  }
}

```

**引用：**[https://www.php.net/manual/en/reflectionextension.getfunctions.php](https://www.php.net/manual/en/reflectionextension.getfunctions.php)