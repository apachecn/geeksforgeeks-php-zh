# PHP 数组如何转换成 JavaScript 或 JSON？

> 原文:[https://www . geesforgeks . org/how-convert-PHP-array-to-JavaScript-or-JSON/](https://www.geeksforgeeks.org/how-to-convert-php-array-to-javascript-or-json/)

PHP 提供了 **[json_encode()函数](https://www.geeksforgeeks.org/php-json_encode-function/)** ，将 PHP 数组转换成 JavaScript。从技术上讲，它是 JSON 格式的。JSON 代表 JS 对象简谱。

**语句:**如果你有一个 PHP 数组，你需要把它转换成 JavaScript 数组，那么有一个 PHP 提供的函数可以很容易地把那个 PHP 数组转换成 JavaScript 数组。但是在使用这个函数之前，您需要做一些事情，首先确保您使用的是 PHP 5.2 或更高版本。接下来，使用库函数 **json_encode()** 将 PHP 数组转换为 JavaScript 数组。

**语法:**

```
json_encode( $my_array );
```

**示例 1:** 本示例使用 json_encode()函数将 PHP 数组转换为 JavaScript JSON 对象。

```
<?php  // Array in php
$myArr = array('Geeks', 'GeeksforGeeks@geeks.com');
?>

<!-- Converting PHP array into JavaScript array -->
<script>
var arr = <?php echo json_encode($myArr); ?>;
document.write(arr[1]);
</script>

<?php  ?>
```

**输出:**

```
GeeksforGeeks@geeks.com

```

**示例 2:** 这里你会看到使用**JSON _ encode($ myar)**将一维 PHP 数组转换成 javaScript 数组。传递 php 数组，然后使用 json_encode，我们将其转换为 javascript 数组。

```
<?php  ?>
<script type='text/javascript'>
<?php
$php_array = array('geeks', 'for', 'geeks');
$js_array = json_encode($php_array);
echo "var javascript_array = ". $js_array . ";\n";
?>
document.write(javascript_array[0]);
</script>

<?php  ?>
```

**输出:**

```
geeks
```

**例 3:** 这里你会看到使用**JSON _ encode($ myar)**将多维 PHP 数组转换成 javaScript 数组。传递 php 数组，然后使用 json_encode，我们将其转换为 javascript 数组。

```
<?php  ?>

<script type='text/javascript'>

<?php
$php_array = array(
   array('Geeks', 'for@example.com'),
   array('for', 'gfg@example.com'),
);
$js_array = json_encode($php_array);
echo "var javascript_array = ". $js_array . ";\n";
?>

document.write(javascript_array[0][1]);
</script>

<?php  ?>
```

**输出:**

```
for@example.com
```

**注意:**需要注意的是，json_encode()函数仅在 PHP 5.2 或更高版本中可用。