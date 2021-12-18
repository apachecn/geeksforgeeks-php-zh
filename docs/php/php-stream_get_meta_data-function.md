# PHP|stream_get_meta_data()函数

> Original: [https://www.geeksforgeeks.org/php-stream_get_meta_data-function/](https://www.geeksforgeeks.org/php-stream_get_meta_data-function/)

Stream_get_meta_data()函数是 PHP 中的一个内置函数，用于从流/文件指针获取头数据或元数据。
**语法：**和

```php
*array* stream_get_meta_data( $stream )
```

**参数：**该函数接受单个参数*$stream*，该参数指定要检索的元数据，该元数据由任何函数 fopen()、fsockopen()和 pfsockopen()创建。
**返回值：**此函数返回包含以下项的数组：

*   **TIMED_OUT：**它是布尔类型的 Items，如果流超时，则为 true。
*   **阻塞：**它是布尔类型的项，如果流处于阻塞 IO 模式，则为 True。
*   **eof(Bool)**它是可选的。 如果流到达文件末尾，则为 True。
*   **unread_bytes：**内部缓冲区中的字节数。
*   **stream_type：**用于指定流的实现。
*   **wrapper_type：**用于指定协议包装器实现层。
*   **Wrapper_Data：**它是附加到此流的特定数据。
*   **模式：**它是此流所需的访问类型。
*   **可查找：**当前流查找时为真。
*   **URI：**用户提供了统一资源标识符。

以下程序说明 PHP：
**程序 1：**和
中的 stream_get_meta_data()函数

## PHP

```php
<?php

// PHP program to illustrate
// stream_get_meta_data function

$url = 'http://php.net/manual/en/function.stream-get-meta-data.php';

$file = fopen($url, 'r');
$meta_data = stream_get_meta_data($file);

print_r($meta_data);

fclose($file);

?>
```

**Output:** 

```php
Array
(
    [timed_out] => 
    [blocked] => 1
    [eof] => 
    [wrapper_data] => Array
        (
            [0] => HTTP/1.1 200 OK
            [1] => Server: nginx/1.10.3
            [2] => Date: Mon, 17 Dec 2018 11:04:39 GMT
            [3] => Content-Type: text/html; charset=utf-8
            [4] => Connection: close
            [5] => Content-language: en
            [6] => X-Frame-Options: SAMEORIGIN
            [7] => Set-Cookie: LAST_LANG=en; expires=Tue, 17-Dec-2019 11:04:39 GMT; Max-Age=31536000; path=/; domain=.php.net
            [8] => Set-Cookie: COUNTRY=NA%2C54.201.119.186; expires=Mon, 24-Dec-2018 11:04:39 GMT; Max-Age=604800; path=/; domain=.php.net
            [9] => Link: ; rel=shorturl
            [10] => Last-Modified: Mon, 17 Dec 2018 05:06:18 GMT
            [11] => Vary: Accept-Encoding
        )

    [wrapper_type] => http
    [stream_type] => tcp_socket/ssl
    [mode] => r
    [unread_bytes] => 7647
    [seekable] => 
    [uri] => http://php.net/manual/en/function.stream-get-meta-data.php
)
```

**程序 2：**打印函数返回的数组长度的程序。

## PHP

```php
<?php

// PHP program to illustrate
// stream_get_meta_data function

// url to be open using fopen
$url = 'http://www.php.net/news.rss';

// checking is url openable or not
if (!$fp = fopen($url, 'r')) {
    trigger_error("Unable to open URL ($url)", E_USER_ERROR);
}

$fp = fopen($url, 'r');

$meta_data = stream_get_meta_data($fp);

print(sizeof($meta_data));

fclose($fp);
?>
```

**Output:** 

```php
10
```

**引用：**[http://php.net/manual/en/function.stream-get-meta-data.php](http://php.net/manual/en/function.stream-get-meta-data.php)