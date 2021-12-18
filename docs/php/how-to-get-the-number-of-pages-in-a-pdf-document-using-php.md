# 如何用 PHP 获取一个 PDF 文档的页数？

> 原文:[https://www . geeksforgeeks . org/如何获取 pdf 文档中的页数-使用-php/](https://www.geeksforgeeks.org/how-to-get-the-number-of-pages-in-a-pdf-document-using-php/)

PHP 提供了内置的函数和扩展，可以用来计算文档的页数。pdf 扩展名。有许多方法可以做到这一点。以下是计算 pdf 文档页数的方法:

**方法一:使用 ImageMagic 扩展:**PHP 提供的扩展是 **ImageMagic** ，能够理解 pdf 文档。用于相同的命令是**“识别”**命令。所以专用于所需目的的完整 PHP 函数是 **Imagick::identifyImage()** 。

**方法二:使用 TCPDI 功能:**另一种方法是使用 **TCPDI** 功能。它不使用任何 PHP 库来执行这个任务。可以使用下面一行代码。

> $pageCount =(新 TCPDI())- > setSourceData((字符串)file _ get _ contents($ fileName))；

**方法三:使用 pdfinfo:** 对于 Linux 用户来说，有一种比“identity”函数更快的统计 pdf 文档页数的方法。下面给出的命令可以用于同样的目的。在执行此命令之前，需要安装 pdfinfo。当 pdf 文档中的页数太大时，此命令的运行速度非常快。对于 Windows 用户，pdfinfo 可以作为 pdfinfo.exe 使用。下面是命令:

> exec('/usr/bin/pdfinfo '。$tmpfname。| awk \'/Pages/ {print $2}\ "，$ output)；

**方法 4:使用 pdf 作为文本文件:**现在，让我们看看 PHP 中的代码，它会告诉我们 pdf 文档中的页数。在这段代码中，我们创建了一个包含逻辑的函数“count”。此外，在变量“路径”中，写入要计算页数的 pdf 的路径。请确保路径写得正确。

```php
<?php 
$path = 'pdf/GFG.pdf';
$totalPages = count($path);

echo $totoalPages;

function count($path) {
  $pdf = file_get_contents($path);
  $number = preg_match_all("/\/Page\W/", $pdf, $dummy);
  return $number;
}  
?>
```

**输出:**

```php
4
```