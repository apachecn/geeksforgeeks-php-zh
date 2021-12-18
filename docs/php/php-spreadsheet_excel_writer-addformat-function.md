# PHP|Spreadsheet_Excel_Writer|addFormat()函数

> Original: [https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-addformat-function/](https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-addformat-function/)

AddFormat()函数是 PHP|Spreadsheet_Excel_Writer 中的内置函数，用于设置电子表格的格式。

**语法：**↔

```
Workbook::&addFormat( $properties = array() )
```

**参数：**此函数接受接受数组值的单个参数*$properties*。 为了设置各种格式，我们使用它们对应的函数，如*setBold()*用于 Bold，*setBorde()*用于边框，以及许多其他函数。

**示例 1：**

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