# PHP|Spreadsheet_Excel_Writer|setItalic()函数

> Original: [https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-setitalic-function/](https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-setitalic-function/)

SetItalic()函数是 PHP|Spreadsheet_Excel_Writer 中的内置函数，用于将字体样式设置为斜体。

**语法：**

```php
*void* Format::setItalic()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 PEAR_ERROR。

**示例 1：**

## PHP

```php
<?php
// require_once 'Spreadsheet/Excel/Writer.php';

// Add Workbook
$workbook = new Spreadsheet_Excel_Writer();

// Add Format to spreadsheet
$format_italic =& $workbook->addFormat();

// Set Italic
$format_italic->setItalic();

// Add Worksheet to Spreadsheet
$worksheet =& $workbook->addWorksheet();

// Write to Worksheet
$worksheet->write(0, 0, "Details of GeeksforGeeks
                      Contributors", $format_italic);
$worksheet->write(1, 0, "Author", $format_italic);
$worksheet->write(1, 1, "User Handle", $format_italic);
$worksheet->write(2, 0, "Sarthak", $format_italic);
$worksheet->write(2, 1, "sarthak_ishu11", $format_italic);

// Send .xlsx file to header
$workbook->send('test.xls');

// Close Workbook Object
$workbook->close();
?>
```

发帖主题：Re：Колибри0.7.0

![](img/12af6cc3593a14bb5fa0734b5541286e.png)

**示例 2：**

## PHP

```php
<?php

// require_once 'Spreadsheet/Excel/Writer.php';

// Create Spreadsheet_Excel_Writer Object
$workbook = new Spreadsheet_Excel_Writer();

// Add Worksheet
$worksheet =& $workbook->addWorksheet();

// Set Font Family Times New Roman
$format_setItalic =& $workbook->addFormat();
$format_setItalic->setFontFamily('Times New Roman');

// Set Italic Property
$format_setItalic->setItalic();

// Set Shadow to text
$format_setItalic->setShadow();

// Write to Worksheet
$worksheet->write(0, 0, "Information");
$worksheet->write(1, 0, "Website Name", $format_setItalic);
$worksheet->write(1, 1, "Address", $format_setItalic);
$worksheet->write(2, 0, "GeeksforGeeks", $format_setItalic);
$worksheet->write(2, 1, "https://www.geeksforgeeks.org/",
                                     $format_setItalic);
$workbook->send('test.xls');

$workbook->close();
?>
```

发帖主题：Re：Колибри0.7.0

![](img/6053fba1d472df4ecc1b0ec91898e0f3.png)

**引用：**[https://pear.php.net/manual/en/package.fileformats.spreadsheet-excel-writer.spreadsheet-excel-writer-format.setitalic.php](https://pear.php.net/manual/en/package.fileformats.spreadsheet-excel-writer.spreadsheet-excel-writer-format.setitalic.php)