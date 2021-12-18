# PHP|Spreadsheet_Excel_Writer|Close()函数

> Original: [https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-close-function/](https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-close-function/)

Close()函数是 PHP|Spreadsheet_Excel_Writer 中的一个内置函数，用于完成完成所有操作后的电子表格。 此方法应该始终是每个工作簿上最后调用的方法。

**语法：**

```
*mixed* Workbook::close()
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