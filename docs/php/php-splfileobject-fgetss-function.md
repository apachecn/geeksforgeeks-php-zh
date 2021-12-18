# PHP|SplFileObject fgetss()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-fgetss-function/](https://www.geeksforgeeks.org/php-splfileobject-fgetss-function/)

**SplFileObject：：fgetss()**函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于从文件中获取行并去除 HTML 标记。
**语法：**

```
string SplFileObject::fgetss( $tags)
```

**参数：**此函数只接受一个参数**$tag**一个可选参数，用于指定不应剥离的标记。
**返回值：**此函数返回去除 HTML 和 PHP 代码的文件的下一行，否则返回 FALSE。
下面的程序演示了 PHP 中的 SplFileObject：：fgetss()函数。
**程序 1：**和

## PHP

```
<?php
$gfg = <<<EOD
<html><body>
 <h1>Welcome To GeeksforGeeks!</h1>
</body></html>

Text out of the HTML block.
EOD;

file_put_contents("gfg.txt", $gfg);

$file = new SplFileObject("gfg.txt");
while (!$file->eof()) {
    echo $file->fgetss();
}
?>
```

发帖主题：Re：Колибри0.7.8.0

```
Welcome To GeeksforGeeks! Text out of the HTML block.
```

**程序 2：**和

## PHP

```
<?php
$gfg = <<<EOD
<html><body>
 <h1>Welcome To GeeksforGeeks!</p>

</body></html>

Text out of the HTML block.
EOD;

file_put_contents(__FILE__, $gfg);

$file = new SplFileObject(__FILE__);
while (!$file->eof()) {
    echo $file->fgetss();
}
?>
```

发帖主题：Re：Колибри0.7.8.0

```
Welcome To GeeksforGeeks! Text out of the HTML block.
```

**引用：**[http://php.net/manual/en/splfileobject.fgets.php](http://php.net/manual/en/splfileobject.fgets.php)