# PHP|SplFileObject eof()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-eof-function/](https://www.geeksforgeeks.org/php-splfileobject-eof-function/)

**SplFileObject：：EOF()**函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于文件末尾。
**语法：**

```
string SplFileObject::eof( void )
```

**参数：**此函数不接受任何参数。

**返回值：**成功时返回 TRUE。

下面的程序演示了 PHP 中的 SplFileObject：：EOF()函数。

**注意：**程序 1 使用了包含以下数据的 gfg.txt 文件。

```
GeeksforGeeks
A Computer Science 
Portal for Geeks
```

**Program 1:**

```
<?php

// Creating SplFile Object
$file = new SplFileObject(__FILE__);

foreach ($file as $gfg => $line) {
   if($file->eof() == true)
        { echo "Yes Reached EOF";
        break;
        }
}
?>
```

发帖主题：Re：Колибри0.7.0

```
Yes Reached EOF

```

**程序 2：**

```
<?php 

// PHP program to use array to check 
// multiple files 

$GFG = array(
    "/home/rajvir/Desktop/GeeksforGeeks/dummy.php",
    "gfg.txt",
    "mime.php"
    );

foreach ($GFG as &$file_name) { 

    // Create new SplFile Object 
    $file = new SplFileObject($file_name); 
    foreach($file as $gfg=>$lines){
    if($file->eof() == true)
        echo "Yes Reached EOF" . "</br>"; 
    }   
} 
?>
```

**Output:**

```
Yes Reached EOF
Yes Reached EOF
Yes Reached EOF

```

**引用：**[http://php.net/manual/en/splfileobject.eof.php](http://php.net/manual/en/splfileobject.eof.php)