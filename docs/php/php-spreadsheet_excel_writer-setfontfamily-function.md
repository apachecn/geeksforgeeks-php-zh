# PHP|Spreadsheet_Excel_Writer|setFontFamily()函数

> Original: [https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-setfontfamily-function/](https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-setfontfamily-function/)

SetFontFamily()函数是 PHP|Spreadsheet_Excel_Writer 中的内置函数，用于设置字体系列。

**语法：**

```
*void* Format::setFontFamily( $font_family )
```

**参数：**此函数接受单个参数*$font_family*。 字体系列名称，可以是“Times New Roman”、“Arial”、“Courier”。
**返回值：**此函数成功时返回 TRUE，失败时返回 PEAR_ERROR。

**示例 1：**

## PHP

```
<?php

require_once 'Spreadsheet/Excel/Writer.php';

// Add Workbook
$workbook = new Spreadsheet_Excel_Writer();

// Add Format to spreadsheet
$format_border =& $workbook->addFormat();

// Add Worksheet to Spreadsheet
$worksheet =& $workbook->addWorksheet();

// Add Format to variable
$format_times =& $workbook->addFormat();

// Set Font Family Times New Roman
$format_times->setFontFamily('Times New Roman');

// Add Format to variable
$format_courier =& $workbook->addFormat();

// Set Font Family Courier
$format_courier->setFontFamily('Courier');

// Write to Worksheet
$worksheet->write(0, 0, "Details of GeeksforGeeks Contributors");
$worksheet->write(1, 0, "Author", $format_times);
$worksheet->write(1, 1, "User Handle", $format_courier);
$worksheet->write(2, 0, "Sarthak");
$worksheet->write(2, 1, "sarthak_ishu11");

// Send .xlsx file to header
$workbook->send('test.xls');

// Close Workbook Object
$workbook->close();
?>
```