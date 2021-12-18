# PHP|Spreadsheet_Excel_Writer|setOutLine()函数

> Original: [https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-setoutline-function/](https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-setoutline-function/)

SetOutLine()函数是 PHP|Spreadsheet_Excel_Writer 中的内置函数，用于设置字体轮廓。

**语法：**

```
*void* Format::setOutLine()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 PEAR_ERROR。

**示例 1：**

## PHP

```
<?php

require_once 'Spreadsheet/Excel/Writer.php';

// Create Spreadsheet_Excel_Writer Object
$workbook = new Spreadsheet_Excel_Writer();

// Add Worksheet
$worksheet =& $workbook->addWorksheet();

// Set Font Family Times New Roman
$format_times =& $workbook->addFormat();
$format_times->setFontFamily('Times New Roman');

// Set Outline
$format_times->setOutLine();

// Set Shadow to text
$format_times->setShadow();

// Write to Worksheet
$worksheet->write(0, 0, "Information");
$worksheet->write(1, 0, "Website Name", $format_times);
$worksheet->write(1, 1, "Address", $format_times);
$worksheet->write(2, 0, "GeeksforGeeks");
$worksheet->write(2, 1, "https://www.geeksforgeeks.org/");
$workbook->send('test.xls');

$workbook->close();
?>
```

发帖主题：Re：Колибри0.7.0

![](img/511637d97171bf7b8aaef1d888df521f.png)

**示例 2：**

## PHP

```
<?php

require_once 'Spreadsheet/Excel/Writer.php';

// Add Workbook
$workbook = new Spreadsheet_Excel_Writer();

// Add Format to spreadsheet
$format_bold =& $workbook->addFormat();

// Set Bold Format
$format_bold->setBold();

// Set Outline
$format_bold->setOutLine();

// Add Worksheet to Spreadsheet
$worksheet =& $workbook->addWorksheet();

$format_bold->setBorder(2);

// Write to Worksheet
$worksheet->write(0, 0, "Details of GeeksforGeeks
                      Contributors", $format_bold);
$worksheet->write(1, 0, "Author", $format_bold);
$worksheet->write(1, 1, "User Handle", $format_bold);
$worksheet->write(2, 0, "Sarthak");
$worksheet->write(2, 1, "sarthak_ishu11");

// Send .xlsx file to header
$workbook->send('test.xls');

// Close Workbook Object
$workbook->close();
?>
```

发帖主题：Re：Колибри0.7.0

![](img/243fa9cc30281f3e1a9f536df5c4d26d.png)

**引用：**[https://pear.php.net/manual/en/package.fileformats.spreadsheet-excel-writer.spreadsheet-excel-writer-format.setoutline.php](https://pear.php.net/manual/en/package.fileformats.spreadsheet-excel-writer.spreadsheet-excel-writer-format.setoutline.php)