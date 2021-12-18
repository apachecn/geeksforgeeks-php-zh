# PHP|xml_parser_get_option()函数

> Original: [https://www.geeksforgeeks.org/php-xml_parser_get_option-function/](https://www.geeksforgeeks.org/php-xml_parser_get_option-function/)

**先决条件：**[XML 基础知识](https://www.geeksforgeeks.org/xml-basics/)

**xml_parser_get_option()函数**是 PHP 中的一个内置函数，用于从 XML 解析器检索选项。

**语法：**

```
*mixed* xml_parser_get_option( *resource* $parser, *int* $specified_option )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$parser：**它是必需的参数。 它指定要检索其选项的 XML 解析器。
*   **$Specified_Option：**必选参数(整数)。 它指定要从指定解析器检索的选项。
    参数的可能值包括：

*   **XML_OPTION_CASE_FOLDING：**用于指定案例折叠。 如果启用，则返回 1；如果禁用，则返回 0。
*   **XML_OPTION_TARGET_ENCODING：**用于指定指定 XML 解析器中的目标编码。 它返回编码的名称(US-ASCII、UTF-8 或 ISO-8859-1 等)。
*   **XML_OPTION_SKIP_TAGSTART：**它用于指定标记名称开头跳过的字符数。
*   **XML_OPTION_SKIP_WHITE：**它用于指定是否跳过由空格字符组成的值。 如果跳过，则返回 1，否则返回 0。

**返回值：**此函数成功时返回指定选项的值，失败时返回 False。

**注：**

*   此函数适用于 PHP 4.0.0 及更新版本。
*   选项参数 XML_OPTION_SKIP_TAGSTART 和 XML_OPTION_SKIP_WHITE 仅适用于 PHP 7.1.0 和更新版本。

**程序 1：**

```
<?php

// Creating an XML parser
$parser = xml_parser_create();

echo "This example illustrates how xml_parser_get_option()"
        . " function works<br>";
echo "XML_OPTION_CASE_FOLDING: " . xml_parser_get_option(
            $parser, XML_OPTION_CASE_FOLDING) ."<br>";

// Free to XML parser
xml_parser_free($parser);

?>
```

发帖主题：Re：Колибри0.7.0

```
This example show how xml_parser_get_option() function works
XML_OPTION_CASE_FOLDING: 1

```

**程序 2：**

```
<?php

// Create an XML parser
$parser = xml_parser_create();

// Getting the option for all possible options
echo "option = XML_OPTION_CASE_FOLDING: " . 
    xml_parser_get_option($parser, XML_OPTION_CASE_FOLDING) ."<br>";

echo "option = XML_OPTION_TARGET_ENCODING: " .
    xml_parser_get_option($parser, XML_OPTION_TARGET_ENCODING) ."<br>";

echo "option = XML_OPTION_SKIP_TAGSTART: " .
    xml_parser_get_option($parser, XML_OPTION_SKIP_TAGSTART) ."<br>";

echo "option = XML_OPTION_SKIP_WHITE: " .
    xml_parser_get_option($parser, XML_OPTION_SKIP_WHITE);

// Free to XML parser
xml_parser_free($parser);

?>
```

发帖主题：Re：Колибри0.7.0

```
option = XML_OPTION_CASE_FOLDING: 1
option = XML_OPTION_TARGET_ENCODING: UTF-8
option = XML_OPTION_SKIP_TAGSTART: 0
option = XML_OPTION_SKIP_WHITE: 0

```

**引用：**[https://www.php.net/manual/en/function.xml-parser-get-option.php](https://www.php.net/manual/en/function.xml-parser-get-option.php)