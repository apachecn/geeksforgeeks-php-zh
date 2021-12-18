# 在 PHP 5 中排序数组

> 原文:[https://www.geeksforgeeks.org/sorting-arrays-php-5/](https://www.geeksforgeeks.org/sorting-arrays-php-5/)

**什么是排序？**
排序是指按照数据项之间的某种线性关系，将数据按字母、数字顺序以及递增或递减的方式进行排序。排序大大提高了搜索效率。

**PHP 中数组的排序函数**

1.  sort()–按升序对数组进行排序
2.  rsort()–按降序对数组进行排序
3.  asort()–根据值以升序对关联数组进行排序
4.  ksort()–根据关键字，以升序对关联数组进行排序
5.  arsort()–根据值以降序对关联数组进行排序
6.  krsort()–根据键以降序对关联数组进行排序

**按升序排序数组–排序()**

以下函数按升序对数值数组的元素进行排序:

```
INPUT :
```

```
<!DOCTYPE html>
<html>
<body>

<?php
$numbers = array(40, 61, 2, 22, 13);
sort($numbers);

$arrlength = count($numbers);
for($x = 0; $x < $arrlength; $x++) {
    echo $numbers[$x];
    echo "<br>";
}
?>

</body>
</html>
```

```
OUTPUT :
```

2
13
22
40
61

**按降序排列数组–rsort()**
以下函数按降序排列数值数组的元素:

```
INPUT :
```

```
<!DOCTYPE html>
<html>
<body>

<?php
$numbers = array(40, 61, 2, 22, 13);
rsort($numbers);

$arrlength = count($numbers);
for($x = 0; $x < $arrlength; $x++) {
    echo $numbers[$x];
    echo "<br>";
}
?>

</body>
</html>
```

```
OUTPUT :
```

61
40
22
13
2

**按值升序排列数组–asort()**
以下函数按值升序排列关联数组:

```
INPUT :
```

```
<!DOCTYPE html>
<html>
<body>

<?php
$age = array("ayush"=>"23", "shankar"=>"47", "kailash"=>"41");
asort($age);

foreach($age as $x => $x_value) {
    echo "Key=" . $x . ", Value=" . $x_value;
    echo "<br>";
}
?>

</body>
</html>
```

```
OUTPUT :
```

Key=Ayush，Value = 23
Key =凯拉什，Value=41
Key=Shankar，Value=47

**按键升序排列数组–ksort()**
以下函数按键升序排列关联数组:

```
INPUT :
```

```
<!DOCTYPE html>
<html>
<body>

<?php
$age = array("ayush"=>"23", "shankar"=>"47", "kailash"=>"41");
ksort($age);

foreach($age as $x => $x_value) {
    echo "Key=" . $x . ", Value=" . $x_value;
    echo "<br>";
}
?>

</body>
</html>
```

```
OUTPUT :
```

Key=Ayush，Value = 23
Key =凯拉什，Value=41
Key=Shankar，Value=47

**按值降序排列数组–arsort()**
以下函数根据值降序排列关联数组。

```
INPUT :
```

```
<!DOCTYPE html>
<html>
<body>

<?php
$age = array("ayush"=>"23", "shankar"=>"47", "kailash"=>"41");
arsort($age);

foreach($age as $x => $x_value) {
    echo "Key=" . $x . ", Value=" . $x_value;
    echo "<br>";
}
?>

</body>
</html>
```

```
OUTPUT :
```

Key=Shankar，Value=47
Key=Kailash，Value=41
Key=Ayush，Value=23

**按键降序排列数组–krsort()**
以下函数按键降序排列关联数组。

```
INPUT :
```

```
<!DOCTYPE html>
<html>
<body>

<?php
$age = array("ayush"=>"23", "shankar"=>"47", "kailash"=>"41");
krsort($age);

foreach($age as $x => $x_value) {
    echo "Key=" . $x . ", Value=" . $x_value;
    echo "<br>";
}
?>

</body>
</html>
```

```
OUTPUT :
```

Key=Shankar，Value=47
Key=Kailash，Value=41
Key=Ayush，Value=23