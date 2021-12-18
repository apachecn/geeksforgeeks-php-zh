# PHP|json_decode()函数

> Original: [https://www.geeksforgeeks.org/php-json_decode-function/](https://www.geeksforgeeks.org/php-json_decode-function/)

Json_decode()函数是 PHP 中的内置函数，用于解码 JSON 字符串。 它将 JSON 编码的字符串转换为 PHP 变量。

**语法：**

```
json_decode( $json, $assoc = FALSE, $depth = 512, $options = 0 )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **json：**它保存需要解码的 JSON 字符串。 它只适用于 UTF-8 编码字符串。
*   **assoc：**它是一个布尔变量。 如果为真，则返回的对象将转换为关联数组。
*   **深度：**它说明用户指定的递归深度。
*   **选项：**包括 JSON_OBJECT_AS_ARRAY、JSON_BIGINT_AS_STRING、、JSON_SHOW_ON_ERROR 的位掩码。

**返回值：**此函数返回适当 PHP 类型的编码 JSON 值。 如果 json 无法解码，或者如果编码的数据比递归限制更深，则返回 NULL。

以下示例说明了 PHP 中 json_decode()函数的用法：
**示例 1：**

```
<?php

// Declare a json string
$json = '{"g":7, "e":5, "e":5, "k":11, "s":19}';

// Use json_decode() function to
// decode a string
var_dump(json_decode($json));

var_dump(json_decode($json, true));

?>
```

**Output:**

```
object(stdClass)#1 (4) {
  ["g"]=>
  int(7)
  ["e"]=>
  int(5)
  ["k"]=>
  int(11)
  ["s"]=>
  int(19)
}
array(4) {
  ["g"]=>
  int(7)
  ["e"]=>
  int(5)
  ["k"]=>
  int(11)
  ["s"]=>
  int(19)
}

```

**示例 2：**

```
<?php

// Declare a json string
$json = '{"geeks": 7551119}';

// Use json_decode() function to
// decode a string
$obj = json_decode($json);

// Display the value of json object
print $obj->{'geeks'};

?>
```

**Output:**

```
7551119

```

**使用 json_decode()函数时的常见错误：**

*   使用的字符串是有效的 JavaScript，但不是有效的 JSON。
*   名称和值必须用双引号括起来，不允许使用单引号。
*   不允许使用尾随逗号。

**引用：**[http://php.net/manual/en/function.json-decode.php](http://php.net/manual/en/function.json-decode.php)