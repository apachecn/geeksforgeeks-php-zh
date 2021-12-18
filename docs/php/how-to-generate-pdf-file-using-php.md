# 如何使用 PHP 生成 PDF 文件？

> 原文:[https://www . geesforgeks . org/如何使用-php 生成-pdf-file/](https://www.geeksforgeeks.org/how-to-generate-pdf-file-using-php/)

在本文中，我们将学习如何使用 **FPDF 用 PHP 生成 PDF 文件。**它是一个免费的 PHP 类，包含了很多创建和修改 pdf 的功能。FPDF 类包括许多功能，如页面格式、页眉、页脚、自动分页符、换行符、图像支持、颜色、链接等。

**进场:**

*   你需要从 [FPDF 网站](http://www.fpdf.org/)下载 FPDF 类，并将其包含在你的 PHP 脚本中。

```php
require('fpdf/fpdf.php');
```

*   根据您的需要实例化并使用 FPDF 类，如下例所示。

```php
$pdf=new FPDF();
```

**示例 1:** 以下示例使用代码中的给定文本生成一个 PDF 文件。可以根据需要下载或预览该文件。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

ob_end_clean();
require('fpdf/fpdf.php');

// Instantiate and use the FPDF class 
$pdf = new FPDF();

//Add a new page
$pdf->AddPage();

// Set the font for the text
$pdf->SetFont('Arial', 'B', 18);

// Prints a cell with given text 
$pdf->Cell(60,20,'Hello GeeksforGeeks!');

// return the generated output
$pdf->Output();

?>
```

**输出:**

![](img/f83fbe34e34f499acabfc88aec5bc064.png)

**示例 2:** 以下示例有助于理解页眉和页脚的设置，以及在 PDF 文件的不同页面上打印多行。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

require('fpdf/fpdf.php');

class PDF extends FPDF {

    // Page header
    function Header() {

        // Add logo to page
        $this->Image('gfg1.png',10,8,33);

        // Set font family to Arial bold 
        $this->SetFont('Arial','B',20);

        // Move to the right
        $this->Cell(80);

        // Header
        $this->Cell(50,10,'Heading',1,0,'C');

        // Line break
        $this->Ln(20);
    }

    // Page footer
    function Footer() {

        // Position at 1.5 cm from bottom
        $this->SetY(-15);

        // Arial italic 8
        $this->SetFont('Arial','I',8);

        // Page number
        $this->Cell(0,10,'Page ' . 
            $this->PageNo() . '/{nb}',0,0,'C');
    }
}

// Instantiation of FPDF class
$pdf = new PDF();

// Define alias for number of pages
$pdf->AliasNbPages();
$pdf->AddPage();
$pdf->SetFont('Times','',14);

for($i = 1; $i <= 30; $i++)
    $pdf->Cell(0, 10, 'line number ' 
            . $i, 0, 1);
$pdf->Output();

?>
```

**输出:**

![](img/aa495f04b8d6cd84c0da19f21c250f73.png)