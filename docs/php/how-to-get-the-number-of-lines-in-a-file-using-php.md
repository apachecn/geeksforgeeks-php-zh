# 如何用 PHP 获取一个文件的行数？

> 原文:[https://www . geesforgeks . org/如何使用 php 获取文件中的行数/](https://www.geeksforgeeks.org/how-to-get-the-number-of-lines-in-a-file-using-php/)

给定一个文件引用，用 PHP 找到这个文件的行数。共有 3 种方法可以解决这个问题。

**test.txt:** 该文件用于测试以下所有 PHP 代码

```php
Geeks
For
Geeks
```

**方法 1:** 将整个文件加载到内存中，然后使用 [**count()**](https://www.geeksforgeeks.org/php-count-function/) 函数返回该文件的行数。

**例:**

## PHP

```php
<?php
    $filePath = "test.txt";
    $lines = count(file($filePath));
    echo $lines;
?>
```

**输出:**

```php
3
```

这种方法将整个文件加载到内存中，这可能会导致内存溢出问题。

**方法 2:** 这里我们一次只加载一行文件，比第一种方法好。PHP [**fopen()**](https://www.geeksforgeeks.org/php-fopen-function-open-file-or-url/) 功能是用来打开一个文件或者 URL。PHP[**fgets()**](https://www.geeksforgeeks.org/php-fgets-function/)**函数用于从打开的文件中返回一行。**[**fclose()**](https://www.geeksforgeeks.org/php-fclose-function/)功能用于关闭文件指针。****

******例:******

## ****PHP****

```php
**<?php
    $filePath="test.txt";
    $linecount = 0;
    $handleFile = fopen($file, "r");
    while(!feof($handleFile)){
      $line = fgets($handleFile);
      $linecount++;
    }

    fclose($handleFile);

    echo $linecount;
?>**
```

******输出:******

```php
**3**
```

****如果 1GB 文件只有一行呢。这段代码将加载整个 1GB 的数据，这可能会导致内存溢出问题。****

******方法 3:** 我们只将特定大小的数据加载到内存中。我们不关心装载时的断线。我们将迭代加载的数据，计算其中的换行符数量。****

******示例:******

## ****PHP****

```php
**<?php
    $filePath="test.txt";
    $linecount = 0;
    $handleFile = fopen($filePath, "r");

    while(!feof($handleFile)){
      // We are loading only 4096 bytes of data at a time.
      $line = fgets($handleFile, 4096);

      // We are using PHP_EOL (PHP End of Line)
      //to count number of line breaks in currently loaded data.
      $linecount = $linecount + substr_count($line, PHP_EOL);
    }

    fclose($handleFile);

    echo $linecount;
?>**
```

******输出:******

```php
**3**
```

****就空间而言，这是一种更好的方法，但是，请注意，我们对数据迭代了两次，因此，所花费的时间将是两倍。****