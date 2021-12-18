# PHP|gmp_Random_Seed()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_random_seed-function/](https://www.geeksforgeeks.org/php-gmp_random_seed-function/)

GMP_RANDOM_SEED()是 PHP 中的一个内置函数，用于设置 RNG 种子([随机数生成](https://en.wikipedia.org/wiki/Random_number_generation))。

**语法：**

```
void gmp_random_seed ( mixed $seed )

```

**参数：**gmp_Random_Seed()函数接受如上所述的单个参数，如下所述：

*   **$Seed:** it is the parameter required by the unique GMP_RANDOM_SEED () function to set for the [gmp_Random ()](http://php.net/manual/en/function.gmp-random.php) , [GMP_RANDOM_RANGE ()](http://php.net/manual/en/function.gmp-random-range.php) , and [GMP_RANDOM_BITS ()](http://php.net/manual/en/function.gmp-random-bits.php) functions. This parameter can be a GMP resource in PHP 5.5 or earlier, a GMP object in PHP 5.6 or later, or you can pass a numeric string, provided that the string can be converted to a number.

**返回值：**函数 GMP_RANDOM_SEED()成功时返回 NULL，失败时返回 FALSE。

**注：**

```
Warning: The function generates an E-Warning and returns False if the seed is not valid.

```

**示例：**下面的程序说明了 PHP 中的 gmp_Random_Seed()函数：

**程序 1：**

```
<?php

// PHP code implementing the gmp_random_seed function

// setting the seed
gmp_random_seed(100);

var_dump(gmp_strval(gmp_random(1)));

?>
```

帖子主题：Re：Колибри

**程序 2：**

```
<?php
//php code implementing the gmp_random_seed() function

// set the seed to something else
gmp_random_seed(gmp_init(-100));

var_dump(gmp_strval(gmp_random_bits(10)));

?>
```

帖子主题：Re：Колибри

**程序 3：**

```
<?php
//PHP code implementing gmp_random_seed() function 

// set the seed to something invalid
var_dump(gmp_random_seed('not a number'));

?>
```

帖子主题：Re：Колибри

**相关文章：**

*   [php|gmp_mod()函数](https://www.geeksforgeeks.org/php-gmp_mod-function/)
*   [php|gmp_Random_Range()函数](https://www.geeksforgeeks.org/php-gmp_random_range-function/)

**引用：**[http://php.net/manual/en/function.gmp-random-seed.php](http://php.net/manual/en/function.gmp-random-seed.php)