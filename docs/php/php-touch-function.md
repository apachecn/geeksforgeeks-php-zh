# PHP|touch()函数

> Original: [https://www.geeksforgeeks.org/php-touch-function/](https://www.geeksforgeeks.org/php-touch-function/)

PHP 中的 touch()函数是一个内置函数，用于设置指定文件的访问和修改时间。
必须设置其访问和修改时间的文件的文件名作为参数与时间一起发送给 touch()函数，成功时返回 True，失败时返回 False。 如果文件不存在，则首先创建该文件。

**语法：**

```php
touch(filename, time, atime)
```

**使用的参数：**
PHP 中的 touch()函数接受三个参数。

1.  **filename：**这是一个必选参数，指定必须更改其访问和修改时间的文件的文件名。
2.  **时间：**可选参数，指定时间，默认为当前系统时间。
3.  **atime：**这是一个可选参数，指定访问时间。 默认情况下，如果未设置参数，则占用当前系统时间。

**返回值：**
成功返回 True，失败返回 False。

**错误和异常**

1.  不同的文件系统的时间分辨率可能不同，因此有时可能会得到意想不到的结果。
2.  Touch()函数中的$time 参数将来的限制在 1000000 秒左右。
3.  目录上使用的 touch()函数返回 FALSE，并在 NTFS 和 FAT 文件系统上打印“Permission Defined”。

**示例：**

```php
Input : $file_pointer = "gfg.txt";
        if (touch($file_pointer)) 
        {
           echo ("$file_pointer modification time has been set to current system time.");
        } 
        else 
        {
           echo ("$file_pointer modification time cannot be changed.");
        }
Output :gfg.txt modification time has been set to current system time.

Input : $file_pointer = "gfg.txt";
        $time = time() - 18000;
        if (touch($file_pointer, $time)) 
        {
           echo ("$file_pointer modification time has been changed to 5 hours in the past.");
        } 
        else 
        {
           echo ("$file_pointer modification time cannot be changed.");
        }

Output : gfg.txt modification time has been changed to 5 hours in the past.

```

下面的程序说明了 touch()函数。

假设有一个名为“gfg.txt”的文件

**程序 1**

```php
<?php
$file_pointer = "gfg.txt";
// using touch() function to change the modification 
// time of a file to current system time
if (touch($file_pointer)) 
{
   echo ("$file_pointer modification time has been set to current system time.");
} 
else 
{
   echo ("$file_pointer modification time cannot be changed.");
}

?>
```

发帖主题：Re：Колибри0.7.0

```php
gfg.txt modification time has been set to current system time.
```

**程序 2**

```php
<?php
$file_pointer = "gfg.txt";

// setting touch time to 5 hours in the past
$time = time() - 18000;

// using touch() function to change the modification 
// time of a file to current system time
if (touch($file_pointer, $time)) 
{
    echo ("$file_pointer modification time has been changed to 5 hours in the past.");
 } 
else 
{
   echo ("$file_pointer modification time cannot be changed.");
}

?>
```

发帖主题：Re：Колибри0.7.0

```php
gfg.txt modification time has been changed to 5 hours in the past.
```

**引用：**
[http://php.net/manual/en/function.touch.php](http://php.net/manual/en/function.touch.php)