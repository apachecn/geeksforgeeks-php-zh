# PHP|pack()函数

> Original: [https://www.geeksforgeeks.org/php-pack-function/](https://www.geeksforgeeks.org/php-pack-function/)

Pack()函数是 PHP 中的内置函数，用于将给定参数打包为给定格式的二进制字符串。

**语法：**

```
pack( $format, $arguments )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$format:** required parameter. It specifies the format to be used when packaging data. Possible format values are:
    *   **empty filled** -string
    *   **-filled in blanks**
    *   ****h** -first hexadecimal string of low-order half-byte**
    *   ****H** -the first hexadecimal string in the high half byte**
    *   ****.****
    *   ******C** -unsigned character****
    *****   **s** -signed short (16 bits, machine byte order)*   **S** -unsigned short (16 bits, machine byte order)*   **n** -unsigned short (16 bits, machine byte order)*   **n** -unsigned short (16 bits, machine byte order). Big end byte order)*   **v** -unsigned short (16 bits). Small end byte order)*   **I** -signed integers (machine-related byte order and size)*   **I** -unsigned integers (machine-related byte order and size)*   **l** -signed long integers (32 bits). Machine byte order)*   **L** -unsigned long integer (32 bits, machine byte order)*   **N** -unsigned Long (32 bits, big-end byte order)*   **V** -unsigned Long (32 bits). Small end byte order)*   **f** -FLOAT (machine-related representation and size)*   **d** -DOUBLE (machine-related representation and size)*   **x** -NUL BYTE*   **X** -back up a byte*   **Z [T89\. Filled***   **@** -nul- filled to absolute position****
*   ****$Arguments:** it is an optional parameter. It specifies one or more parameters to package.**

****返回值：**返回包含数据的二进制字符串。**

****注意：**此函数在 PHP 4.0.0 及更新版本中可用。**

****程序 1：**本程序使用**C**格式来格式化输入参数。**

```
<?php
echo pack("C13", 71, 69, 69, 75, 83, 70, 79, 82, 71, 69, 69, 75, 83);
?>
```

****输出：**

```
GEEKSFORGEEKS

```** 

****程序 2：**本程序使用**A**格式来格式化输入参数。**

```
<?php
echo pack("A3", 71898);
?>
```

****输出：**

```
718

```** 

****程序 3：**本程序使用**I**格式来格式化输入参数。**

```
<?php
echo pack("i3", 56, 49, 54);
?>
```

****输出：**

```
816

```** 

****引用：**[https://www.php.net/manual/en/function.pack.php](https://www.php.net/manual/en/function.pack.php)**