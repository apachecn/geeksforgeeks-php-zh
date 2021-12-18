# PHP|xml_parse_into_struct()函数

> Original: [https://www.geeksforgeeks.org/php-xml_parse_into_struct-function/](https://www.geeksforgeeks.org/php-xml_parse_into_struct-function/)

**xml_parse_into_struct()函数**是 PHP 中的内置函数，用于将 XML 数据解析为数组结构。 XML 数据被解析成两个并行数组结构，第一个是**索引数组**，它包含指向值数组中的值位置的指针，第二个是**值数组**，它包含来自解析的 XML 的数据。

**语法：**

```
*int* xml_parse_into_struct( *resource* $xml_parser, *string* $data,
                                        *array* $values, *array* $index )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$xml_parser：**它是必需的参数。 它包含 XML 解析器的引用。
*   **$data：**必选参数。 它保存包含 XML 数据的字符串。
*   **$Values：**必选参数。 它保存包含 XML 数据值的数组。
*   **$index：**可选参数。 它指定一个数组，该数组带有指向$VALUES 中的值位置的指针。

**返回值：**此函数成功时返回 1，失败时返回 0。 它与 True and False 不同。

**注：**

*   此函数适用于 PHP 4.0.0 及更新版本。
*   这些示例可能在在线 IDE 上不起作用。 因此，尝试在本地服务器或 php 托管服务器上运行它。

加入时间：清华大学 2007 年 01 月 25 日下午 3：33

## 可扩展标记语言

```
<?xml version="1.0" encoding="utf-8"?>
<user>
    <username> user123 </username>
    <name> firstname lastname </name>
    <phone> +91-9876543210 </phone>
    <detail> I am John Doe. Live in Kolkata, India. </detail>
</user>
```

**程序 1：**

## PHP

```
<?php

// Create an xml parser
$xml_parser = xml_parser_create();

// Opening xml file in file stream
$filePointer = fopen("sample.xml", "r");

// Reading XML data from the
// specified XML file
$xml_data = fread($filePointer, 4096);

// Parsing XML data into an
// array structure
xml_parse_into_struct($xml_parser,
                $xml_data, $values);

// Free to xml parse
xml_parser_free($xml_parser);

// Display array structured XML data
print_r($values);

// Closing the XML file
fclose($filePointer);

?>
```

发帖主题：Re：Колибри0.7.0

```
Array
(
    [0] => Array
        (
            [tag] => USER
            [type] => open
            [level] => 1
            [value] => 
        )
    [1] => Array
        (
            [tag] => USERNAME
            [type] => complete
            [level] => 2
            [value] =>  user123 
        )
    [2] => Array
        (
            [tag] => USER
            [value] => 
            [type] => cdata
            [level] => 1
        )
    [3] => Array
        (
            [tag] => NAME
            [type] => complete
            [level] => 2
            [value] =>  firstname lastname 
        )
    [4] => Array
        (
            [tag] => USER
            [value] => 
            [type] => cdata
            [level] => 1
        )
    [5] => Array
        (
            [tag] => PHONE
            [type] => complete
            [level] => 2
            [value] =>  +91-9876543210 
        )
    [6] => Array
        (
            [tag] => USER
            [value] => 
            [type] => cdata
            [level] => 1
        )
    [7] => Array
        (
            [tag] => DETAIL
            [type] => complete
            [level] => 2
            [value] =>  I am John Doe. Live in Kolkata, India. 
        )
    [8] => Array
        (
            [tag] => USER
            [value] => 
            [type] => cdata
            [level] => 1
        )
    [9] => Array
        (
            [tag] => USER
            [type] => close
            [level] => 1
        )
)
```

加入时间：清华大学 2007 年 01 月 25 日下午 3：33

## 可扩展标记语言

```
<?xml version="1.0"?>
<atoms>
    <atom>
        <name>Carbon</name>
        <symbol>C</symbol>
        <atomic_no>6</atomic_no>
    </atom>
    <atom>
        <name>Hydrogen</name>
        <symbol>H</symbol>
        <atomic_no>1</atomic_no>
    </atom>
    <atom>
        <name>Helium</name>
        <symbol>He</symbol>
        <atomic_no>2</atomic_no>
    </atom>
    <atom>
        <name>Iron</name>
        <symbol>Fe</symbol>
        <atomic_no>26</atomic_no>
    </atom>
</atoms>
```

**程序 2：**

## PHP

```
<?php

class Atom {
    var $name;  // Name of the element
    var $symbol;    // Symbol for the atom
    var $atomic_no;  // Atomic number

    // Constructor for Atom class
    function __construct( $aa ) {

        // Initializing or setting the values
        // to the field of the Atom class
        foreach ($aa as $k=>$v)
            $this->$k = $aa[$k];
    }
}

function read_data($filename) {

    // Read the XML database of atoms
    $xml_data = implode("", file($filename));

    // Creating an xml parser
    $xml_parser = xml_parser_create();

    xml_parser_set_option($xml_parser, XML_OPTION_CASE_FOLDING, 0);
    xml_parser_set_option($xml_parser, XML_OPTION_SKIP_WHITE, 1);
    xml_parse_into_struct($xml_parser, $xml_data, $values, $tags);

    // Free to xml parser
    xml_parser_free($xml_parser);

    // Iterating through the structures
    foreach ($tags as $key=>$val) {

        if ($key == "atom") {

            $atom_ranges = $val;

            // Each contiguous pair of array entries
            // are the lower and upper range for
            // each molecule definition
            for($i = 0; $i < count($atom_ranges); $i += 2) {
                $offset = $atom_ranges[$i] + 1;
                $len = $atom_ranges[$i + 1] - $offset;

                // Parsing atom data
                $tdb[] = parseAtoms(array_slice($values, $offset, $len));
            }
        }
        else {
            continue;
        }
    }
    return $tdb;
}

// parseAtoms function to parse atom
function parseAtoms($mvalues) {
    for ($i = 0; $i < count($mvalues); $i++) {
        $ato[$mvalues[$i]["tag"]] = $mvalues[$i]["value"];
    }
    return new Atom($ato);
}

$db = read_data("atoms.xml");
echo "Database of atoms objects:\n";
print_r($db);

?>
```

发帖主题：Re：Колибри0.7.0

```
Database of atoms objects:
Array
(
    [0] => Atom Object
        (
            [name] => Carbon
            [symbol] => C
            [atomic_no] => 6
        )
    [1] => Atom Object
        (
            [name] => Hydrogen
            [symbol] => H
            [atomic_no] => 1
        )
    [2] => Atom Object
        (
            [name] => Helium
            [symbol] => He
            [atomic_no] => 2
        )
    [3] => Atom Object
        (
            [name] => Iron
            [symbol] => Fe
            [atomic_no] => 26
        )
)
```

**引用：**[https://www.php.net/manual/en/function.xml-parse-into-struct.php](https://www.php.net/manual/en/function.xml-parse-into-struct.php)