# 如何在 PHP 中获取一个模块的所有函数名？

> 原文:[https://www . geesforgeks . org/如何获取 php 中模块的所有函数名/](https://www.geeksforgeeks.org/how-to-get-all-function-names-of-a-module-in-php/)

在本文中，我们将学习如何获取 PHP 模块中所有函数的名称。

**PHP 中什么是模块？**

模块是独立软件组件的集合。程序中模块的使用提高了代码的可重用性和封装性。模块包含函数，我们可以通过在代码中包含该模块来使用这些函数。现在我们要打印给定模块中的所有函数。

**如何在 PHP 中获取一个模块所有函数的名称？**

要获取一个 PHP 模块的所有函数的名称，我们可以使用 **get_extension_funcs()** 函数。该函数将模块名作为输入参数，并将函数名数组作为输出返回。

**示例 1:** 在本例中，我们将打印 JSON 模块中存在的所有函数。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

$func_names = get_extension_funcs("DOM");
$length = count($func_names);

for($i = 0; $i < $length; $i++) {
    echo($func_names[$i]);
    echo("<br>");
}
?>
```

**Output**

```
dom_import_simplexml
```

**示例 2:** 在本例中，我们将打印 XML 模块中存在的所有函数。**T3】**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

$func_names = get_extension_funcs("XML");
$length = count($func_names);

for($i = 0; $i < $length; $i++) {
    echo($func_names[$i]);
    echo("<br>");
}
?>
```

**Output**

```
xml_parser_create
xml_parser_create_ns
xml_set_object
xml_set_element_handler
xml_set_character_data_handler
xml_set_processing_instruction_handler
xml_set_default_handler
xml_set_unparsed_entity_decl_handler
xml_set_notation_decl_handler
xml_set_external_entity_ref_handler
xml_set_start_namespace_decl_handler
xml_set_end_namespace_decl_handler
xml_parse
xml_parse_into_struct
xml_get_error_code
xml_error_string
xml_get_current_line_number
xml_get_current_column_number
xml_get_current_byte_index
xml_parser_free
xml_parser_set_option
xml_parser_get_option
utf8_encode
utf8_decode
```

**示例 3:** 在本例中，我们将打印 DOM 模块中存在的所有函数。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

$func_names = get_extension_funcs("JSON");
$length = count($func_names);

for($i = 0; $i < $length; $i++) {
    echo($func_names[$i]);
    echo("<br>");
}
?>
```

**Output**

```
json_encode
json_decode
json_last_error
json_last_error_msg
```