# PHP|Spreadsheet_Excel_Writer|send()函数

> Original: [https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-send-function/](https://www.geeksforgeeks.org/php-spreadsheet_excel_writer-send-function/)

Send()函数是 PHP|Spreadsheet_Excel_Writer 中的内置函数，用于发送具有正确内容类型(application/vnd.ms-excel)、缓存控制和文件名的 HTTP 标头。

**语法：**

```php
*void* Spreadsheet_Excel_Writer::send( $filename )
```

**参数：**此函数接受作为*$filename*的单个参数，该参数接受要发送到标头的文件的名称。

**返回值：**此函数成功时返回 TRUE，失败时返回 PEAR_ERROR。

**示例 1：**

```php
<?php

// require_once 'Spreadsheet/Excel/Writer.php';

// Add object of class Spreadsheet_Excel_Writer
$workbook = new Spreadsheet_Excel_Writer();
$worksheet =& $workbook->addWorksheet();

// Add a format to the workbook
$format_align =& $workbook->addFormat();

// Set color for the text 
$format_align->setColor ('green');

// Set alignment of text to the center of the cell 
$format_align->setAlign('center');

// Set alignment of text to the center from the top of the cell 
$format_align->setAlign('vcenter');

// Add boldness to the text 
$format_align->setBold(1);

// Set size of the text
$format_align->setSize(25);

// Add data to the cell
$worksheet->write(0, 5, 'GeeksforGeeeks!', $format_align);
$worksheet->write(1, 5, 'A Computer Science Portal For Geeks', $format_align);

// Send HTTP headers with the content-type (application/vnd.ms-excel)
$workbook->send('test.xlsx');

// Free the memory
$workbook->close();
?>
```

**输出：**
![](img/46794eab0dd4981f6f748c74ab48fb9f.png)

**示例 2：**

```php
<?php

// require_once 'Spreadsheet/Excel/Writer.php';

// Add object of class Spreadsheet_Excel_Writer
$workbook = new Spreadsheet_Excel_Writer();
$worksheet =& $workbook->addWorksheet();

// Add Format to the workbook
$format_align =& $workbook->addFormat();

// Set Color for the text 
$format_align->setColor ('white');

// Set Alignment of text to the top of the cell 
$format_align->setAlign('top');

// Set Alignment of text to the right of the cell 
$format_align->setAlign('right');

// Set background color
$format_align->setBgColor('black');

// Set Pattern to the cell
$format_align->setPattern(1);

// Add Boldness to the text 
$format_center->setItalic(1);

// Set Size of the text
$format_align->setSize(20);

// Add data to the cell
$worksheet->write(7, 5, 'Sarthak Prajapati', $format_align);
$worksheet->write(8, 5, 'sarthak_ishu11', $format_align);
$worksheet->write(9, 5, 'Chandigarh', $format_align);

// Send HTTP headers with the content-type (application/vnd.ms-excel)
$workbook->send('test.xlsx');

// Free the memory
$workbook->close();
?>
```

**输出：**
![](img/5ea0d42de70c5cb552d920e5b9e74e05.png)

**引用：**[https://pear.php.net/manual/en/package.fileformats.spreadsheet-excel-writer.spreadsheet-excel-writer.send.php](https://pear.php.net/manual/en/package.fileformats.spreadsheet-excel-writer.spreadsheet-excel-writer.send.php)