# PHP|parse_url()函数

> Original: [https://www.geeksforgeeks.org/php-parse_url-function/](https://www.geeksforgeeks.org/php-parse_url-function/)

Parse_url()函数是 PHP 中的一个内置函数，用于通过解析返回 URL 的组件。 它解析 URL 并返回包含其各种组件关联数组。

**语法：**

```
parse_url( $url, $component = -1 )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **url:** this parameter holds the URL to be parsed. Invalid characters are replaced with _ (underscore).
*   **component:** this parameter specifies that any component (PHP_URL_SCHEME, PHP_URL_HOST, PHP_URL_PORT, PHP_URL_USER, PHP_URL_PASS, PHP_URL_PATH, PHP_URL_QUERY, or PHP_URL_FRANMENT) retrieves a specific URL as a string.

**返回值：**

*   If the Component parameter is omitted, an associative array is returned.
*   If a component parameter is specified, a string is returned.
*   Returns FALSE if the parameter is a malformed URL.

以下示例说明了 PHP 中 parse_url()函数的使用：

**示例 1：**

```
<?php

// Declare a variable and initialize it with URL
$url = 'http://geeksforgeeks.org/php/#basics';

// Use parse_url() function to parse the URL
var_dump(parse_url($url));
var_dump(parse_url($url, PHP_URL_SCHEME));

?>
```

**输出：**

```
array(4) {
  ["scheme"]=>
  string(4) "http"
  ["host"]=>
  string(17) "geeksforgeeks.org"
  ["path"]=>
  string(5) "/php/"
  ["fragment"]=>
  string(6) "basics"
}
string(4) "http"

```

**示例 2：**

```
<?php

// Declare a variable and initialize it with URL
$url = '//www.geeksforgeeks.org/path?php=PHP';

// Use parse_url() function to
// parse the URL
var_dump(parse_url($url));

?>
```

**输出：**

```
array(3) {
  ["host"]=>
  string(21) "www.geeksforgeeks.org"
  ["path"]=>
  string(5) "/path"
  ["query"]=>
  string(7) "php=PHP"
}

```

**引用：**[http://php.net/manual/en/function.parse-url.php](http://php.net/manual/en/function.parse-url.php)