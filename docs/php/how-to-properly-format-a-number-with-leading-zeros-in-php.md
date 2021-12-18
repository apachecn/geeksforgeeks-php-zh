# PHP 中如何正确格式化前导零的数字？

> 原文:[https://www . geesforgeks . org/如何在 php 中正确格式化带前导零的数字/](https://www.geeksforgeeks.org/how-to-properly-format-a-number-with-leading-zeros-in-php/)

数字本质上是堆叠在一起形成整数或字符串的数字序列。数字可以以前导零开始。也可以循环一个数字，并可以进行修改，将另一个字符序列附加或连接到其中。

**方法 1:使用 for 循环进行字符串连接**

可以迭代 for 循环，其中迭代次数等于前导零的个数。在每次迭代过程中，字符串的前面会附加一个零。时间复杂度就零的数量而言是线性的，并且被假定为对于所有实际目的都是恒定的。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
    #declaring the number of zeros to lead the number
    $no_of_zeros = 4;
    #declaring the number
    $number = 999;
    print ("Original number : ");
    print ($number."\n"."<br>");
    #leading the number with indicated zeros
    for($i=1;$i<=$no_of_zeros;$i++)
    {
      #concatenating 0 string in front of number
      $number = '0'.$number;
    }
    print ("Modified number : ");
    print ($number);
?>
```

**Output**

```php
Original number : 999
Modified number : 0000999
```

**方法 2:整数到字符串的转换**

字符串变量可以用来代替存储数字。不必明确指定数字的长度。PHP 自动强制存储号码的类型。此外，数据类型的显式更改可以通过将类型转换为所需的格式来实现。

但是，数字数据类型在存储数字时有一个限制，即没有任何前导零，因此，一旦完成转换，所有的零都会被移除。下面的代码片段演示了这个过程。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
  #declaring a number using a string with leading zeros
  $num = "00000092939292";

  #printing the number
  echo "Original Number \n";
  echo $num."\n"."<br>";
  echo "explicit casting.\n";

  #explicit casting
  echo (int)$num;
?>
```

**Output**

```php
Original Number 
00000092939292
explicit casting.
92939292
```

**方法三:使用**[**str _ pad()**](https://www.geeksforgeeks.org/php-str_pad-function/)**方法**

此方法将字符串填充到指定字符的新长度。在这种情况下，数字是使用字符串变量声明的。如果指定的长度小于或等于字符串的原始长度，则不对原始字符串进行任何修改。 *str_pad()* 方法是执行重复字符串连接的另一种替代方法。

在这种方法中，我们将使用左填充从左侧填充字符串。 *pad_type* 为 STR_PAD_LEFT， *pad_string* 相当于“0”。长度等于原始字符串的长度加上我们希望在数字前面加的零的数量。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
#specify the new length of the string
$len = 8;

#declare number using a string
$str = "2222";
echo("Original String \t");
echo ($str."\n");

#compute new string
$new_str = str_pad($str,$len,"0", STR_PAD_LEFT);
echo("Modified String \t");
echo $new_str;
?>
```

**Output**

```php
Original String     2222
Modified String     00002222
```

**方法 4:使用** [**格式说明符**](https://www.geeksforgeeks.org/php-format-specifiers/)**printf()/sprintf()**

函数的作用是:产生一个格式化的字符串。根据前导字符和字符串的总长度，指定输出数字的格式。需要指出数字的类型，即是十进制、十六进制还是八进制等等。它用于修改数字，以反映数字的正确模式。调用此函数时，至少有一个参数是必需的。

**语法:**

```php
printf(format,arg1,arg2)
```

**参数:**

*   格式(必需):格式化变量的字符串。
*   arg1:要插入第一个%符号的值
*   arg2(可选):要插入第二个%符号的值

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
  #declaring the number
  $num = 86857658;
  print("Original Number : ");
  print($num."\n"."<br>");

  #specifying the number of zeros
  $num_of_zeros = 10;

  #defining the total length of the number of
  #zeros and length of the number
  $length = $num_of_zeros + strlen($num) ;

  #defining the character to lead the number with
  $ch = 0;

  #specifying the type of number
  $num_type = 'd';

  #specifying the format
  $format_specifier = "%{$ch}{$length}{$num_type}";

  # print and echo
  print("Modified Number : ");
  printf($format_specifier, $num);

?>
```

**Output**

```php
Original Number : 86857658
<br>Modified Number : 000000000086857658
```