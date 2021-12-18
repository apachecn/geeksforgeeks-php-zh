# PHP|DOMDocument createProcessingInstruction()函数

> Original: [https://www.geeksforgeeks.org/php-domdocument-createprocessinginstruction-function/](https://www.geeksforgeeks.org/php-domdocument-createprocessinginstruction-function/)

**DOMDocument：：createProcessingInstruction()函数**是 PHP 中的内置函数，用于创建 DOMProcessingInstruction 类的新实例。

**语法：**

```php
*DOMProcessingInstruction* DOMDocument::createProcessingInstruction( $target, $data )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$target:** this parameter holds the target of the processing instruction.
*   **$DATA:** this parameter saves the contents of the processing instruction.

**返回值：**此函数成功时返回新的 DOMProcessingInstruction 值，失败时返回 False。

下面的程序说明了 PHP 中的 DOMDocument：：createProcessingInstruction()函数：

**程序 1：**

```php
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createProcessingInstruction() function to create
// a new Processing Instruction node
$domPI = $domDocument->createProcessingInstruction("name", "GeeksforGeeks");

// Append element to the document
$domDocument->appendChild($domPI);

// Create XML document and display it
echo $domDocument->saveXML();

?>
```

**输出：**

```php
<?xml version="1.0" encoding="iso-8859-1"?>
<?name GeeksforGeeks?>

```

**程序 2：**

```php
<?php

// Create a new DOMDocument
$domDocument = new DOMDocument('1.0', 'iso-8859-1');

// Use createProcessingInstruction() function to create
// a new Processing Instruction node
$domPI1 = $domDocument->createProcessingInstruction("name",
                     "GeeksforGeeks");
$domPI2 = $domDocument->createProcessingInstruction("contact",
                     "Noida");
$domPI3 = $domDocument->createProcessingInstruction("email",
                     "abc@geeksforgeeks.org");

// Append element to the document
$domDocument->appendChild($domPI1);
$domDocument->appendChild($domPI2);
$domDocument->appendChild($domPI3);

// Create XML document ans display it
echo $domDocument->saveXML();

?>
```

**输出：**

```php
<?xml version="1.0" encoding="iso-8859-1"?>
<?name GeeksforGeeks?>
<?contact Noida?>
<?email abc@geeksforgeeks.org?>

```

**引用：**[https://www.php.net/manual/en/domdocument.createprocessinginstruction.php](https://www.php.net/manual/en/domdocument.createprocessinginstruction.php)