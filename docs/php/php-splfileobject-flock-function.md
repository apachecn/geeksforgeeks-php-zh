# PHP|SplFileObject flock()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-flock-function/](https://www.geeksforgeeks.org/php-splfileobject-flock-function/)

SplFileObject flock()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于对文件应用可移植锁定。

**语法：**

```
*bool* SplFileObject::flock( $opr, $isBlock )
```

**参数：**此函数接受上述两个参数，如下所述：
**$opr：**它用于从以下列表中指定要应用的操作：

*   LOCK_SH：获取共享锁(读取器)。
*   Lock_ex：获取独占锁(编写器)。
*   LOCK_UN：释放锁。
*   LOCK_NB：锁定时不阻塞。

**$isBlock：**如果锁定被阻止，则此参数设置为 True。

**返回值：**此函数成功时返回 True On，失败时返回 False。

**注意：**请确保以下程序中使用的文件名为 gfg.txt，并且应该具有读写权限。

下面的程序演示了 PHP 中的 SplFileObject：：Flock()函数：

**程序 1：**

```
<?php

// Create Spl Object
$file = new SplFileObject("gfg.txt", "w");

// Add an Exclusive lock to gfg.txt
if ($file->flock(LOCK_SH)) { 
    $file->ftruncate(0);
    $file->fwrite("Write GFG inside the gfg.txt");

    // Release the lock  
    $file->flock(LOCK_UN);
    echo "Success Lock and Unlock Operation";
} 
else {
    echo "No Lock Available";
}
?>
```

发帖主题：Re：Колибри0.7.0

```
Success Lock and Unlock Operation.

```

**程序 2：**

```
<?php

// Create SplFile Object
$file = new SplFileObject("gfg.txt", "w");

// Add an Exclusive lock to gfg.txt
if ($file->flock(LOCK_EX)) { 
    $file->ftruncate(0);
    $file->fwrite("Write GFG inside the gfg.txt");

    // Release the lock  
    $file->flock(LOCK_UN);
    echo "Success Exclusive Lock and Unlock Operation";
} else {
    echo "No Lock Available";
}
?>
```

发帖主题：Re：Колибри0.7.0

```
Success Exclusive Lock and Unlock Operation
```

**引用：**[http://php.net/manual/en/splfileobject.flock.php](http://php.net/manual/en/splfileobject.flock.php)