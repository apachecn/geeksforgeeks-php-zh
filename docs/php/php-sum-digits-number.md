# PHP|数字的位数和

> Original: [https://www.geeksforgeeks.org/php-sum-digits-number/](https://www.geeksforgeeks.org/php-sum-digits-number/)

这是一个简单的 PHP 程序，我们需要在其中计算一个数字的所有数字的总和。
示例：

```
Input : 711 
Output : 9

Input : 14785
Output : 25

```

在本程序中，我们将尝试接受字符串形式的数字，然后遍历字符串的长度。 在迭代过程中，我们将从每个位置提取数字，然后将它们与之前提取的数字相加，从而得到总和。

```
<?php
// PHP program to calculate the sum of digits
function sum($num) {
    $sum = 0;
    for ($i = 0; $i < strlen($num); $i++){
        $sum += $num[$i];
    }
    return $sum;
}

// Driver Code
$num = "711";
echo sum($num);
?>
```

产出：

```
9

```