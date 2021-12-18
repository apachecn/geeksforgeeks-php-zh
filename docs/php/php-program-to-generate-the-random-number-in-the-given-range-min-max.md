# 在给定范围(min，max)

内生成随机数的 PHP 程序

> Original: [https://www.geeksforgeeks.org/php-program-to-generate-the-random-number-in-the-given-range-min-max/](https://www.geeksforgeeks.org/php-program-to-generate-the-random-number-in-the-given-range-min-max/)

随机数可以通过多种方式生成，其中一些在密码上是安全的，另一些则不是。 像 rand()和 Random_int()这样的内置函数可以用来获取某个范围内的随机数。

**[使用 rand()函数：](https://www.geeksforgeeks.org/php-rand-function/)**rand()函数生成介于给定范围或 0 和默认最大值(getgramax())之间的伪随机数，具体取决于系统。

**语法：**

```php
int rand( $min, $max )
```

**参数：**rand()函数接受上述和下面描述的两个可选参数。

*   **$min：**可选参数，用于设置随机数的下限。 MIN 的默认值为 0。
*   **$max：**可选参数，用于设置随机数的上限。 Max 的默认值是 getgragmax()的返回值，这取决于系统(对于 Windows，返回值为 32767)。

**程序 1：**使用 rand()函数生成随机数的 PHP 程序。

```php
<?php
// PHP program to generate random number
// in given range

// Generating Random numbers without range
// rand() function return the random number
$num1 = rand();

echo "Random number: " . $num1 . "\n";

// Generating Random numbers in given range
$num2 = rand(7, 100);

echo "Random number in range (7, 100): ", $num2;

?>
```

**Output:**

```php
Random number: 77551982
Random number in range (7, 100): 37

```

**注：**rand()函数是伪随机函数，表示它从机器获取种子并根据种子生成数字。 因此，数字生成方法不是完全随机的。 这在一定程度上是可以追踪到的。 所以它在密码上是不安全的。 它不用于随机化非常重要的密码学。 要生成加密安全的随机数，请使用 Random_int()函数。

**[使用 Random_int()函数：](https://www.geeksforgeeks.org/php-random_int-function/)**Random_int()函数用于生成加密安全的随机数。 这些数字可以用于无偏见的结果。 Windows 中的函数 CryptGenRandom()和 Linux 中的 getRandom(2)系统调用以生成随机数。

**语法：**

```php
int random_int( $min, $max )
```

**参数：**Random_int()函数接受两个参数，如上所述，如下所述。

*   **$min：**它保持随机数的下限。
*   **$max：**它保持随机数的上限。

**程序 2：**使用 Random_int()函数生成某个范围内的随机数。

```php
<?php
// PHP program to generate random number
// in given range

// Generating Random numbers in given range
// using random_int() function
$num1 = random_int(35, 100);

echo "Random number in range (35, 100): " . $num1 . "\n";

// Random number in range (10, 30)
$num2 = random_int(10, 30);

echo "Random number in range (10, 30): " . $num2;

?>
```

**Output:**

```php
Random number in range (35, 100): 93
Random number in range (10, 30): 28

```