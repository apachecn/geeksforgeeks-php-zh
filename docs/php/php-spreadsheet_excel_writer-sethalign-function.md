# PHP|Spreadsheet_Excel_Writer|setHAlign()函数

> Original: [https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-sethalign-function/](https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-sethalign-function/)

SetHAlign()函数是 PHP|Spreadsheet_Excel_Writer 中的内置函数，用于设置电子表格的单元格对齐方式。

**语法：**

```php
*void* Format::setHAlign( $location )
```

**参数：**此函数接受作为*$location*的单个参数，该参数接受文本放置位置为‘Left’、‘Center’、‘Right’、‘Fill’、‘Justify’、‘Merge’、‘EQUAL_SPACE’。

**返回值：**此函数成功时返回 TRUE，失败时返回 PEAR_ERROR。

**示例 1：**

```php
<?php

// require_once 'Spreadsheet/Excel/Writer.php';

// Add object of class Spreadsheet_Excel_Writer
$workbook = new Spreadsheet_Excel_Writer();
$worksheet =& $workbook->addWorksheet();

// Add a format to the workbook
$format_center =& $workbook->addFormat();

// Set color for the text 
$format_center->setColor ('green');

// Set alignment of text to the center of the cell 
$format_center->setHAlign('center');

// Add boldness to the text 
$format_center->setBold(1);

// Set size of the text
$format_center->setSize(25);

// Add data to the cell
$worksheet->write(0, 5, 'GeeksforGeeeks!', $format_center);
$worksheet->write(1, 5, 'A Computer Science Portal For Geeks',
                  $format_center);

// Send file to the browser
$workbook->send('test.xlsx');

// Free the memory
$workbook->close();
?>
```

**输出：**
![](img/8fc4575a1e496402e42242b8f7a3f16f.png)

**示例 2：**

```php
<?php
// require_once 'Spreadsheet/Excel/Writer.php';

// Add object of class Spreadsheet_Excel_Writer
$workbook = new Spreadsheet_Excel_Writer();
$worksheet =& $workbook->addWorksheet();

// Add a Format to the workbook
$format_center =& $workbook->addFormat();

// Set Color for the text 
$format_center->setColor ('white');

// Set Alignment of text to the right of the cell 
$format_center->setHAlign('right');

// Set background color
$format_center->setBgColor('black');

// Set Pattern to the cell
$format_center->setPattern(1);

// Add Boldness to the text 
$format_center->setItalic(1);

// Set Size of the text
$format_center->setSize(20);

// Add data to the cell
$worksheet->write(7, 5, 'Sarthak Prajapati', $format_center);
$worksheet->write(8, 5, 'sarthak_ishu11', $format_center);
$worksheet->write(9, 5, 'Chandigarh', $format_center);

// Send file to the browser
$workbook->send('test.xlsx');

// Free the memory
$workbook->close();
?>
```

**输出：**
![](img/3e39f3188137166a2d9372e34c614804.png)

**引用：**[https://pear.php.net/manual/en/package.fileformats.spreadsheet-excel-writer.spreadsheet-excel-writer-format.sethalign.php](https://pear.php.net/manual/en/package.fileformats.spreadsheet-excel-writer.spreadsheet-excel-writer-format.sethalign.php)