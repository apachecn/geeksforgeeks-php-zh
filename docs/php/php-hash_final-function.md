# PHP|HASH_FINAL()函数

> Original: [https://www.geeksforgeeks.org/php-hash_final-function/](https://www.geeksforgeeks.org/php-hash_final-function/)

Hash_inal()函数是 PHP 中的一个内置函数，用于完成增量散列并返回结果摘要。

**语法：**

```php
hash_final( $context, $raw_output )
```

**参数：**此函数接受上述两个参数，如下所述。

*   **$CONTEXT:** this parameter is used to specify the hash context returned by the hash_init () function.
*   **$RAW_OUTPUT:** this parameter is used to set a Boolean value. If this parameter is set to True, the output contains raw binary data; if the parameter is set to False, the output contains lowercase hexadecimal.

**返回值：**此函数以小写十六进制返回包含计算出的消息摘要的字符串。

下面的程序演示了 PHP 中的 hash_inal()函数：

**程序 1：**

```php
<?php

// PHP program too illustrate 
// hash_final function
$gfg = hash_init('md5');

hash_update($gfg, 'GeeksforGeeks A CS Portal');

// Print result return by
// hash_final function
print(hash_final($gfg));
?>
```

**输出：**

```php
a26b1748ffd7e4c9923336a3c8e9a4c3

```

**程序 2：**

```php
<?php

// PHP program too illustrate 
// hash_final function
$gfg = hash_init('md5');

hash_update($gfg, 'GeeksforGeeks A CS Portal');

// Print result return by
// hash_final function
print(hash_final($gfg, false));
?>
```

**输出：**

```php
a26b1748ffd7e4c9923336a3c8e9a4c3

```

**引用：**[http://php.net/manual/en/function.hash-final.php#refsect1-function.hash-final-parameters](http://php.net/manual/en/function.hash-final.php#refsect1-function.hash-final-parameters)