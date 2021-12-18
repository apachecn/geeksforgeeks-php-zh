# PHP|Spreadsheet_Excel_Writer|setBold()函数

> Original: [https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-setbold-function/](https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-setbold-function/)

SetBold()函数是 PHP|Spreadsheet_Excel_Writer 中的内置函数，用于设置文本的粗体。

**语法：**

```
*void* Format::setBold( $weight = 1 )
```

**参数：**此函数接受单个参数*$weight*，该参数用于设置文本的粗细。 文本粗细的默认值为 1(700)。 它的范围从 100 到 1000。

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
$format_setBold =& $workbook->addFormat();
$format_setBold->setFontFamily('Times New Roman');

// Set Bold Property
$format_setBold->setBold();

// Set Shadow to text
$format_setBold->setShadow();

// Write to Worksheet
$worksheet->write(0, 0, "Information");
$worksheet->write(1, 0, "Website Name", $format_setBold);
$worksheet->write(1, 1, "Address", $format_setBold);
$worksheet->write(2, 0, "GeeksforGeeks", $format_setBold);
$worksheet->write(2, 1, "https://www.geeksforgeeks.org/",
                                      $format_setBold);
$workbook->send('test.xls');

$workbook->close();
?>
```

发帖主题：Re：Колибри0.7.0

![](img/7e45c20170f749b15ddcd1d59096fcd3.png)

**示例 2：**

## PHP

```
<?php
require_once 'Spreadsheet/Excel/Writer.php';

// Add Workbook
$workbook = new Spreadsheet_Excel_Writer();

// Add Format to spreadsheet
$format_bold =& $workbook->addFormat();

// Set Bold
$format_bold->setBold();

// Add Worksheet to Spreadsheet
$worksheet =& $workbook->addWorksheet();

// Write to Worksheet
$worksheet->write(0, 0, "Details of GeeksforGeeks
                          Contributors", $format_bold);
$worksheet->write(1, 0, "Author", $format_bold);
$worksheet->write(1, 1, "User Handle", $format_bold);
$worksheet->write(2, 0, "Sarthak", $format_bold);
$worksheet->write(2, 1, "sarthak_ishu11", $format_bold);

// Send .xlsx file to header
$workbook->send('test.xls');

// Close Workbook Object
$workbook->close();
?>
```

发帖主题：Re：Колибри0.7.0

![](img/be5026c18df724abf30b88e8c73a450f.png)

**引用：**[https://pear.php.net/manual/en/package.fileformats.spreadsheet-excel-writer.spreadsheet-excel-writer-format.setbold.php](https://pear.php.net/manual/en/package.fileformats.spreadsheet-excel-writer.spreadsheet-excel-writer-format.setbold.php)