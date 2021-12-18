# PHP|JsonSerializable jsonSerialize()函数

> Original: [https://www.geeksforgeeks.org/php-jsonserializable-jsonserialize-function/](https://www.geeksforgeeks.org/php-jsonserializable-jsonserialize-function/)

**JsonSerializable：：jsonSerialize()函数**是 PHP 中的一个内置函数，用于将 JSON 对象序列化为可以使用 json_encode()函数本地序列化的值。

**语法：**

```php
*mixed* JsonSerializable::jsonSerialize( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回 json_encode()函数序列化的数据。

下面的程序演示了 PHP 中的 JsonSerializable：：jsonSerialize()函数：

**程序 1：**

```php
<?php 
class vector implements JsonSerializable { 
    public function __construct(array $arr) { 
        $this->array = $arr; 
    } 

    public function jsonSerialize() { 
        return $this->array; 
    } 
} 

// Declare an array 
$arr = [1, 2, 3, 4, 5]; 

echo("JSON elements:\n"); 

// Convert the array element into JSON
echo json_encode(new vector($arr), JSON_PRETTY_PRINT); 

?> 
```

**输出：**

```php
JSON elements:
[
    1,
    2,
    3,
    4,
    5
]

```

**程序 2：**

```php
<?php 
class vector implements JsonSerializable { 
    public function __construct(array $arr) { 
        $this->array = $arr; 
    } 

    public function jsonSerialize() { 
        return $this->array; 
    } 
} 

// Declare an array 
$arr = [
    "x" => "geeks", 
    "y" => "for",
    "z" => "geeks"
]; 

echo("Convert the array element into JSON:\n"); 

// Convert the array element into JSON
echo json_encode(new vector($arr), JSON_PRETTY_PRINT); 

?> 
```

**输出：**

```php
Convert the array element into JSON:
{
    "x": "geeks",
    "y": "for",
    "z": "geeks"
}

```

**引用：**[https://www.php.net/manual/en/jsonserializable.jsonserialize.php](https://www.php.net/manual/en/jsonserializable.jsonserialize.php)