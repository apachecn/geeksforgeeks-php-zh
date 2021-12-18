# PHP|http_build_query()函数

> Original: [https://www.geeksforgeeks.org/php-http_build_query-function/](https://www.geeksforgeeks.org/php-http_build_query-function/)

**http_build_query()**函数是 PHP 中的一个内置函数，用于从关联(或索引)数组生成 URL 编码的查询字符串。

**语法：**

```php
*string* http_build_query( $query_data, $numeric_prefix, $arg_separator, $enc_type = PHP_QUERY_RFC1738 )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$query_data:** this parameter saves an array or object that contains the following attributes:
    *   It can be an one-dimensional array or a multi-dimensional array.
    *   If $QUERY_DATA is an object, only public properties are merged into the result.
*   **$NUMERIC_PREFIX:** if you use a numeric index in a base array, this parameter will only take precedence over the numeric index of the elements in the base array.
*   **$Arg_Separator:** it is used to separate parameters, but can be overridden by specifying this parameter.
*   **$enc_type:** default value is PHP_QUERY_RFC1738.

**返回值：**它返回 URL 编码的字符串。

下面的程序演示了 PHP 中的 http_build_query()函数：

**程序 1：**

```php
<?php
$info = array(
    'sudo' => 'placement',
    'CPP' => 'course',
    'FORK' => 'C',
);

echo http_build_query($info) . "#";
echo http_build_query($info, '', '&');

?>
```

**输出：**

```php
sudo=placement&CPP=course&FORK=C#sudo=placement&CPP=course&FORK=C

```

**程序 2：**

```php
<?php
$info = array('geeks', 'gfg' => 'sudo', 'placement' => 'hypertext processor');

echo http_build_query($info) . "{content}quot;;
echo http_build_query($info, 'myvar_');
?>
```

**输出：**

```php
0=geeks&gfg=sudo&placement=hypertext+processor$myvar_0=geeks&gfg=sudo&placement=hypertext+processor

```

**引用：**[http://docs.php.net/manual/da/function.http-build-query.php](http://docs.php.net/manual/da/function.http-build-query.php)