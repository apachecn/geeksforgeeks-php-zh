# PHP|exif_tagname()函数

> Original: [https://www.geeksforgeeks.org/php-exif_tagname-function/](https://www.geeksforgeeks.org/php-exif_tagname-function/)

**exif_tagname()函数**是 PHP 中的一个内置函数，用于获取索引头名称。

**语法：**

```php
*string* exif_tagname( *int* $index )
```

**参数：**此函数接受保存头名称的单个参数**$index**。

**返回值：**如果成功，此函数返回 Header 的名称。

下面的示例说明了 PHP 中的**exif_tagname()函数**：

**示例 1：**

```php
<?php

for ($i = 0; $i < 300; $i++) {

    // Get the header
    $header = exif_tagname($i);
    if ($header != '') {
        echo "$i is for "
         . exif_tagname($i) . '<br>';
    }
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```php
<?php

$i = 100;
$j = 256;

// Call to the checker function
checkHeader($i);
checkHeader($j);

// Functiont to check if a header
// is defined or not
function checkHeader($index) {
    $header = exif_tagname($index);

    if($header == '') {
        echo $index . ': This tag is not defined <br>';
     } else {
        echo $index . ': This tag is for '
             . $header . '<br>';
     }
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.exif-tagname.php](https://www.php.net/manual/en/function.exif-tagname.php)