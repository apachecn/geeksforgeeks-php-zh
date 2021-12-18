# 如何用 PHP 将小写字符串转换成大写？

> 原文:[https://www . geesforgeks . org/如何使用-php/](https://www.geeksforgeeks.org/how-to-convert-lowercase-string-to-uppercase-using-php/) 将小写字符串转换为大写字符串

字符串是 PHP 中包含字符、数字或特殊符号的存储对象。PHP 中的字符串区分大小写。使用 PHP 中的各种内置方法，可以很容易地完成小写和大写之间的相互转换。

**方法 1:使用 chr()方法:**这种方法使用各种内置的 PHP 方法将字符串转换为大写字符。最初，字符串由字符、数字或特殊符号组成。str_split()方法用于将字符串转换为单个字符的数组。字符被一起映射到特定的索引以形成字符数组。

然后在这个数组上执行 for 循环迭代。验证每个字符，以验证是否是小写字母字符。ctype_lower()方法用于根据字符所属的类别返回布尔值。这个方法返回真，如果指定的参数字符是小写，否则返回假。

```php
ctype_lower(ch)
```

在这种情况下，该方法返回 FALSE，该字符是非字母字符或大写字符。如果出现这种情况，角色将显示为未修改。否则，通过从其 ASCII 值中减去“32”，将特定字符转换为大写字符。

```php
ord (ch ) - 32
```

然后使用 chr()方法将该整数值转换为相应的字符值。

这种方法执行所需的时间复杂度是 O(l)，其中 l 是字符串的长度。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

 // Declare string
$str = "Geeks^for+Geeks";
print ("Original String \n");

// Split string in characters
$chars = str_split($str);
print ($str. "\n");
print ("Uppercase String \n");

// Looping over characters
foreach ($chars as $ch){

  // Check if character is 
  // small case alphabet
  if(ctype_lower($ch)){

     // Convert to upper case
       echo chr(ord($ch)-32);
  }
  else{

    // Else print character
    // unmodified
    echo($ch);
  }
}
?>
```

**Output**

```php
Original String 
Geeks^for+Geeks
Uppercase String 
GEEKS^FOR+GEEKS
```

**方法二:使用 strtopol()方法:**strtopol()是 PHP 中一个进行大小写转换的内置方法。字母表都被转换成大写字母，并以字符串的形式返回。数字和特殊符号保持不变。结果必须保存在变量中，以便保留更改。与以前的方法相比，这种方法速度更快，并且得到了优化。

```php
strtoupper ( $string ) 
```

**论据:**

$ str–要转换大小写的字符串

**返回类型:**

返回包含所有大写字符的字符串。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
$str = "Geeks^for+Geeks";
print ("Original String \n");
print ($str. "\n");
$cap_str = strtoupper($str);
print ("Uppercase String \n");
print ($cap_str);

?>
```

**Output**

```php
Original String 
Geeks^for+Geeks
Uppercase String 
GEEKS^FOR+GEEKS
```