# PHP|fputcsv()函数

> Original: [https://www.geeksforgeeks.org/php-fputcsv-function/](https://www.geeksforgeeks.org/php-fputcsv-function/)

PHP 中的*fputcsv()*函数是一个内置函数，用于将行格式化为 CSV(逗号分隔值)文件，并将其写入打开的文件。 必须读取的文件和字段作为参数发送给*fputcsv()*函数，如果成功则返回写入字符串的长度，如果失败则返回 False。

**语法：**

```
*int* fputcsv ( $file, $fields, $separator, $enclosure )

```

**参数：**PHP 中的*fputcsv()*函数接受四个参数，如下所述。

*   **$FILE：**它是指定文件的强制参数。
*   **$field：**这是一个强制参数，指定要从哪个数组获取数据。
*   **$分隔符：**这是一个可选参数，用于指定字段分隔符。 默认情况下，fputcsv()函数使用逗号。
*   **$enclosion：**这是一个可选参数，用于指定字段封闭字符。 默认情况下，*fputcsv()*函数使用。

**返回值：**此函数成功时返回写入字符串的长度，失败时返回 False。

**例外：**

*   如果字段中包含封闭字符，则将通过将其加倍来对其进行转义，除非紧跟在其前面的是转义字符。
*   启用 AUTO_DETECT_LINE_ENDINS 运行时配置选项可能有助于解决 PHP 在读取 Macintosh 计算机上或由 Macintosh 计算机创建的文件时正确识别行尾的问题。

下面的程序说明了*fputcsv()*函数：
**程序 1：**

```
<?php
// Sample data for formatting in CSV format
$employees = array("Raj, Singh, Developer, Mumbai",
                    "Sameer, Pandey, Tester, Bangalore",
                    "Raghav, Chauhan, Manager, Delhi");

// opening the file "data.csv" for writing
$myfile = fopen("gfg.csv", "w");

// formatting each row of data in CSV format 
// and outputting it
foreach ($employees as $line)
{
    fputcsv($myfile, explode(',',$line));
}

// closing the file
fclose($myfile); 
?>
```

产出：

```
Raj, Singh, Developer, Mumbai
Sameer, Pandey, Tester, Bangalore
Raghav, Chauhan, Manager, Delhi

```

**程序 2：**

```
<?php
// Sample data for formatting in CSV format
$random_data = array(
array("abc, efg, jhi, klm"),
array("123, 456, 789"),
array("11aa, 22bb, 33cc, 44dd")
);

// opening the file "data.csv" for writing
$myfile = fopen("gfg.csv", "w");

// formatting each row of data in CSV format 
// and outputting it
foreach ($random_data as $line)
{
    fputcsv($myfile, $line);
}

// closing the file
fclose($myfile);
?>
```

产出：

```
abc, efg, jhi, klm
123, 456, 789
11aa, 22bb, 33cc, 44dd

```

**引用：**[http://php.net/manual/en/function.fputcsv.php](http://php.net/manual/en/function.fputcsv.php)