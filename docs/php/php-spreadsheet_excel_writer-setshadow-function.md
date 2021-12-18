# PHP|Spreadsheet_Excel_Writer|setShadow()函数

> Original: [https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-setshadow-function/](https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-setshadow-function/)

SetShadow()函数是 PHP|Spreadsheet_Excel_Writer 中的内置函数，用于将字体设置为阴影。

**语法：**

```
*void* Format::setShadow()
```

**参数：**此函数不接受任何参数。

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

// Set Shadow to text
$format_times->setShadow();

// Add Format to variable
$format_courier =& $workbook->addFormat();

// Set Font Family Courier
$format_courier->setFontFamily('Courier');

// Set Shadow to text
$format_courier->setShadow();

// Write to Worksheet
$worksheet->write(0, 0, "Details of GeeksforGeeks
                    Contributors", $format_times);
$worksheet->write(1, 0, "Author", $format_times);
$worksheet->write(1, 1, "User Handle", $format_times);
$worksheet->write(2, 0, "Sarthak", $format_times);
$worksheet->write(2, 1, "sarthak_ishu11", $format_times);

// Send .xlsx file to header
$workbook->send('test.xls');

// Close Workbook Object
$workbook->close();
?>
```

发帖主题：Re：Колибри0.7.0

![](img/70aea467c398cbbedf00441c3bd863b4.png)

**示例 2：**

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

![](img/e9f5fac8242b47baa6ee94bf6b8c0178.png)

**引用：**[https://pear.php.net/manual/en/package.fileformats.spreadsheet-excel-writer.spreadsheet-excel-writer-format.setshadow.php](https://pear.php.net/manual/en/package.fileformats.spreadsheet-excel-writer.spreadsheet-excel-writer-format.setshadow.php)