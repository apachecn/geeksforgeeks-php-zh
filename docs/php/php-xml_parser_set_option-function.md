# PHP|xml_parser_set_option()函数

> Original: [https://www.geeksforgeeks.org/php-xml_parser_set_option-function/](https://www.geeksforgeeks.org/php-xml_parser_set_option-function/)

**先决条件：**[XML 基础知识](https://www.geeksforgeeks.org/xml-basics/)

**xml_parser_set_option()函数**是 PHP 中的内置函数，用于设置 XML 解析器中的选项。

**语法：**

```php
*bool* xml_parser_set_option( *resource* $parser,
           *int* $specified_option, *mixed* $option_value)
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$parser：**必选参数，指定要设置选项的 XML 解析器。
*   **$Specified_Option：**它是必需的参数，指定要为指定解析器设置的选项。
    此参数的可能值为：

*   **XML_OPTION_CASE_FOLDING：**用于检查是否启用了案例折叠。 值 1 表示启用，值 0 表示禁用值。
*   **XML_OPTION_TARGET_ENCODING：**它指定指定 XML 解析器中的目标编码。 设置编码名称(US-ASCII、UTF-8 或 ISO-8859-1 等)。
*   **XML_OPTION_SKIP_TAGSTART：**它指定在标记名的开头跳过的字符数。
*   **XML_OPTION_SKIP_White：**检查是否跳过空格字符。 值 1 用于跳过，否则为 0。

*   **$option_value:** It is required parameter which specifies that a new value for the specified option to be set.

    **返回值：**成功返回 True，失败返回 False。

    **注意：**此函数适用于 PHP 4.0.0 及更新版本。

    **程序 1：**

    ```php
    <?php

    // Creating XML parser
    $parser = xml_parser_create();

    // Set the option XML_OPTION_CASE_FOLDING
    $res = xml_parser_set_option($parser, XML_OPTION_CASE_FOLDING, 0);

    if( $res ){

        // On success
        echo "option XML_OPTION_CASE_FOLDING has successfully been set!<br>";
    }
    else {

        // On failure
        echo "error while setting option XML_OPTION_CASE_FOLDING!<br>";
    }

    // Setting the option XML_OPTION_TARGET_ENCODING
    $res = xml_parser_set_option($parser, XML_OPTION_TARGET_ENCODING, 'UTF-8');

    if($res) {

        // On success
        echo "option XML_OPTION_TARGET_ENCODING has successfully been set!";
    }
    else {

        // On failure
        echo "error while setting option XML_OPTION_TARGET_ENCODING!";
    }

    // Free to XML parser
    xml_parser_free($parser);

    ?>
    ```

    发帖主题：Re：Колибри0.7.0

    ```php
    option XML_OPTION_CASE_FOLDING has successfully been set!
    option XML_OPTION_TARGET_ENCODING has successfully been set!

    ```

    **程序 2：**本程序显示错误值的结果。

    ```php
    <?php

    // Creating an XML parser
    $parser = xml_parser_create();

    // Setting the option XML_OPTION_TARGET_ENCODING
    $res = xml_parser_set_option($parser, XML_OPTION_TARGET_ENCODING, '0');

    if($res) {

        // On success
        echo "option XML_OPTION_TARGET_ENCODING has successfully been set!";
    }
    else {

        // On failure
        echo "error while setting option XML_OPTION_TARGET_ENCODING!";
    }

    // Free to XML parser
    xml_parser_free($parser);

    ?>
    ```

    **注意：**本例将出现运行时错误，因为该值对于该选项无效。
    **输出：**

    ```php
    error while setting option XML_OPTION_TARGET_ENCODING!

    ```

    **引用：**[https://www.php.net/manual/en/function.xml-parser-set-option.php](https://www.php.net/manual/en/function.xml-parser-set-option.php)