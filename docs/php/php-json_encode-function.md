# PHP|json_encode()函数

> Original: [https://www.geeksforgeeks.org/php-json_encode-function/](https://www.geeksforgeeks.org/php-json_encode-function/)

函数**json_encode()**是 PHP 中的内置函数，用于将 PHP 数组或对象转换为 JSON 表示形式。
**语法：**

```php
*string* json_encode( $value, $option, $depth )
```

**参数：**

*   **$value：**必选参数，定义要编码的值。
*   **$OPTION：**定义由*JSON_FORCE_OBJECT、JSON_HEX_QUOT、JSON_HEX_TAG、JSON_HEX_AMP、JSON_HEX_APOS、JSON_INVALID_UTF8_IGNORE、JSON_INVALID_UTF8_SUBPLECT、JSON_NUMERIC_CHECK、JSON_PARTIAL_OUTPUT_ON_ERROR、JSON_PARTIAL_OUTPUT_ON_ERROR 组成的位掩码的可选参数。*
*   **$Depth：**设置最大深度的可选参数。 它的值必须大于零。

**返回值：**此函数成功时返回 JSON 表示，失败时返回 False。

**示例 1：**此示例将 PHP 数组编码为 JSON 表示形式。

```php
<?php

// Declare an array 
$value = array(
    "name"=>"GFG",
    "email"=>"abc@gfg.com");

// Use json_encode() function
$json = json_encode($value);

// Display the output
echo($json);

?>
```

**Output:**

```php
{"name":"GFG","email":"abc@gfg.com"}

```