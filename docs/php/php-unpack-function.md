# PHP|unpack()函数

> Original: [https://www.geeksforgeeks.org/php-unpack-function/](https://www.geeksforgeeks.org/php-unpack-function/)

Unpack()函数是 PHP 中的一个内置函数，用于将二进制字符串解压缩为相应的格式。

**语法：**

```
*array* unpack( $format, $data, $offset )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$format:** required parameter. It specifies the format to be used when packaging data.
    *   A-represents a string without padding.
    *   A-represents a string filled with spaces.
    *   H-represents the first hexadecimal string of the low-order half-byte.
    *   H-represents the first hexadecimal string in the high half byte.
    *   C-represents signed characters.
    *   C-represents unsigned characters.
    *   S-represents a signed short code (16 bits, machine byte order).
    *   S-represents an unsigned short code (16 bits, machine byte order).
    *   N-represents an unsigned short code (16 bits, big-end byte order).
    *   V-represents an unsigned short code (16 bits, small byte order).
    *   I-represents a signed integer (byte order and size associated with the machine).
    *   I-represents an unsigned integer (byte order and size associated with the machine).
    *   L-represents a signed long integer (32 bits, machine byte order).
    *   L-represents an unsigned long integer (32 bits, machine byte order).
    *   N-represents unsigned length (32 bits, big-end byte order).
    *   V-represents unsigned length (32 bits, small end byte order).
    *   F-represents a floating point (the representation and size associated with the machine).
    *   D-represents double precision (the representation and size associated with the machine).
    *   X-represents NUL bytes.
    *   X-means go back one byte.
    *   Z-represents a string without padding.
    *   @-indicates that the NUL is populated to the absolute position.
*   **$data:** required parameters. It specifies the binary data to unpack.
*   **offset:** this parameter saves the offset from the beginning of unpacking.

**返回值：**成功时返回包含解包元素的关联数组，失败时返回 False。

**注意：**此函数适用于 PHP 4.0.0 及更新版本。

示例 1：此程序使用 C 格式将数据从二进制字符串解包。

```
<?php

var_dump( unpack("C*", "GEEKSFORGEEKS"));
?>
```

**输出：**

```
array(13) {
  [1]=>
  int(71)
  [2]=>
  int(69)
  [3]=>
  int(69)
  [4]=>
  int(75)
  [5]=>
  int(83)
  [6]=>
  int(70)
  [7]=>
  int(79)
  [8]=>
  int(82)
  [9]=>
  int(71)
  [10]=>
  int(69)
  [11]=>
  int(69)
  [12]=>
  int(75)
  [13]=>
  int(83)
}

```

**示例 2：**

```
<?php

$binary_data = pack("c2n2", 0x1634, 0x3623, 65, 66);
var_dump(unpack("c2chars/n2int", $binary_data));
?>
```

**输出：**

```
array(4) {
  ["chars1"]=>
  int(52)
  ["chars2"]=>
  int(35)
  ["int1"]=>
  int(65)
  ["int2"]=>
  int(66)
}

```

**示例 3：**此示例使用 I 格式将数据从二进制字符串解包。

```
<?php

$binary_data = pack("i3", 56, 49, 54);
var_dump(unpack("i3", $binary_data));
?>
```

**输出：**

```
array(3) {
  [1]=>
  int(56)
  [2]=>
  int(49)
  [3]=>
  int(54)
}

```

**引用：**[https://www.php.net/manual/en/function.unpack.php](https://www.php.net/manual/en/function.unpack.php)