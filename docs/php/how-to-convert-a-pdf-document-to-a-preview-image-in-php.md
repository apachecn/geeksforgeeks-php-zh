# 如何在 PHP 中将一个 PDF 文档转换成预览图像？

> 原文:[https://www . geesforgeks . org/how-convert-a-pdf-document-a-preview-image-in-PHP/](https://www.geeksforgeeks.org/how-to-convert-a-pdf-document-to-a-preview-image-in-php/)

将一个 PDF 文档转换成一组图像听起来可能不那么有趣，但它可以有一些应用程序。由于图像中的内容无法轻易复制，这种转换使得文档严格地“只读”，并为防止抄袭提供了额外的保护。当您需要一些现成的幻灯片用于快速办公室演示或将其嵌入到报告和博客中时，这些图像也可能会派上用场。
然而，在这篇文章中，我们将自己局限于一个小得多的例子，即从给定的 PDF 文档生成图像预览。“为什么要预览？”，你可能会问。嗯，一个人可能需要它来做他的图书馆管理系统，她的在线电子书零售店，或者只是为了一些疯狂的周末编程挑战。你认为你可以在你的项目中使用这个概念吗？请在评论中告诉我。
现在从零开始实现完整的转换算法是不可行的，所以我们会坚持第三方库来缓解我们的任务。我发现这个场景中吸引人的方法是基于以下工具:

*   **Ghostscript:** 这是一个命令行工具，适用于所有三个主要平台，即。Windows、Linux 和 Mac，解释 PostSript 和 PDF 文件。你可以在它的[官方网站](https://www.ghostscript.com/doc/9.22/WhatIsGS.htm)上了解更多。
*   **ImageMagick:** 它是一个免费的开源软件套件，用于显示、转换和编辑光栅图像和矢量图像文件。它适用于大多数主流编程语言，包括 PHP。以下是[快速概览](http://php.net/manual/en/book.imagick.php)的标准文档。

### 使用 Ghostscript

要在项目中使用 Ghostscript，请从安装开始。如果您在 windows 上，请从其下载页面下载可执行文件。
Linux 用户可以通过自己默认的包管理器直接安装 Ghostscript

```
# RPM based distros, Fedora 26/27/28
$ sudo dnf install ghostscript
```

通过此命令
验证安装

```
$ gs --version
```

安装后，移动到包含 PDF 文件的目录，并运行以下命令。

```
$ gs -dSAFER -dBATCH -sDEVICE=jpeg \
-dTextAlphaBits=4 -dGraphicsAlphaBits=4 \ 
-dFirstPage=1 -dLastPage=1 -r300 \
-sOutputFile=preview.jpg input.pdf
```

这将从文档中生成第一页的图像。让我们了解它实际上是做什么的；

*   **-SDE 设备:**设置图像的输出文件格式。
*   **-sTEXTVAL，-sGRAPHICVAL:** 设置合成图像的抗锯齿。允许的值是 1、2 和 4。
*   **-r{NUM}:** 设置图像的分辨率(以 dpi 为单位)。
*   **-sFirstPage，-sLastPage:** 设置需要渲染的文档的第一页和最后一页。
*   **-sOutputFile:** 设置输出文件的名称。
*   **input.pdf:** 是用于转换的实际 pdf 文档。

现在为了在 PHP 中使用这个命令，我们调用 exec()函数。例如:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

exec( "ls -l", $output_str, $return_val );

foreach ( $output_str as $line ) {
    echo $line . "\n";
}

?>;
```

这个例子，在 Linux 上，将执行 ls 命令并列出控制台上的所有目录和文件。
我们可以使用这个概念，从 PHP 代码中执行 *ghostscript* 命令。以下是我是如何做到的；

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

function is_pdf ( $file ) {
    $file_content = file_get_contents( $file );

    if ( preg_match( "/^%PDF-[0-1]\.[0-9]+/", $file_content ) ) {
        return true;
    }
    else {
        return false;
    }
}

function create_preview ( $file ) {
    $output_format = "jpeg";
    $antialiasing = "4";
    $preview_page = "1";
    $resolution = "300";
    $output_file = "preview.jpg";

    $exec_command  = "gs -dSAFER -dBATCH -dNOPAUSE -sDEVICE=" . $output_format . " ";
    $exec_command .= "-dTextAlphaBits=". $antialiasing . " -dGraphicsAlphaBits=" . $antialiasing . " ";
    $exec_command .= "-dFirstPage=" . $preview_page . " -dLastPage=" . $preview_page . " ";
    $exec_command .= "-r" . $resolution . " ";
    $exec_command .= "-sOutputFile=" . $output_file . " '" . $file . "'";

    echo "Executing command...\n";
    exec( $exec_command, $command_output, $return_val );

    foreach( $command_output as $line ) {
        echo $line . "\n";
    }

    if ( !$return_val ) {
        echo "Preview created successfully!!\n";
    }
    else {
        echo "Error while creating the preview.\n";
    }
}

function __main__() {
    global $argv;
    $input_file = $argv[1];

    if ( is_pdf( $input_file ) ) {
        // Create preview for the pdf
        create_preview( $input_file );
    }
    else {
        echo "The input file " . $input_file . " is not a valid PDF document.\n";
    }
}

__main__();

?>
```

执行从 __main__()开始，它在命令行获取 PDF 文件。它检查输入文件是否是有效的 PDF。如果有效，它将在输入文件上执行 *ghostscript* 命令。
**输出:**

```
$ php pdf_preview.php input.pdf
Executing command...
GPL Ghostscript 9.22 (2017-10-04)
Copyright (C) 2017 Artifex Software, Inc.  All rights reserved.
This software comes with NO WARRANTY: see the file PUBLIC for details.
Processing pages 1 through 1.
Page 1
Preview created successfully!!
```

### 使用 ImageMagick

像往常一样，我们将从在系统中安装 ImageMagick 二进制文件开始。从依赖项开始；

```
$ sudo dnf install gcc php-devel php-pear
```

之后，安装 ImageMagick

```
$ sudo dnf install ImageMagick ImageMagick-devel
```

然后安装 PHP 包装类；

```
$ sudo pecl install imagick
$ sudo bash -c "echo "extension=imagick.so" > /etc/php.d/imagick.ini"
```

如果你打算在 LAMP 架构上使用它，可以考虑重启 Apache Web 服务器；

```
$ sudo service httpd restart
```

现在我们的系统已经准备好了，我们可以在示例项目中使用 ImageMagick。脚本的基本功能保持不变。您所要做的就是用下面的代码替换 create_preview()函数的内容。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
function create_preview ( $file ) {
    $output_format = "jpeg";
    $preview_page = "1";
    $resolution = "300";
    $output_file = "imagick_preview.jpg";

    echo "Fetching preview...\n";
    $img_data = new Imagick();
    $img_data->setResolution( $resolution, $resolution );
    $img_data->readImage( $file . "[" . ($preview_page - 1) . "]" );
    $img_data->setImageFormat( $output_format );

    file_put_contents( $output_file, $img_data, FILE_USE_INCLUDE_PATH );
}
```

代码是不言自明的。我们正在定义一个 Imagick 类型的实例，并设置各种参数，如分辨率、文件格式等。您要渲染的 PDF 页面作为数组索引出现在文件名之后。例如:

```
First page: input.pdf[0]
Second page: input.pdf[1]
.
.
.
Nth page: input.pdf[N - 1]
```

**输出:**

```
$ php pdf_preview.php input.pdf
Fetching preview...
```

你们中的一些人可能想知道为什么要使用这个方法而不是上一个。我发现 ImageMagick 与 PHP 代码非常一致。编程中的命令行看起来没那么好，有时理解起来会变得臭名昭著。但是，使用相同的配置集，Ghostscript 生成的图像文件比 ImageMagick 渲染的图像文件要小。我不确定这是否是因为一些优化问题，但区别并不是那么大的问题。选择一个还是另一个仅仅是基于你自己的品味。
这就是如何为给定的 PDF 文档创建预览。我希望你从这篇文章中学到了一些新东西。你喜欢哪种方法？对进一步的改进有什么建议吗？欢迎在评论中提及。