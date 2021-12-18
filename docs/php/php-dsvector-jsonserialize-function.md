# PHP|ds\Vector jsonSerialize()函数

> Original: [https://www.geeksforgeeks.org/php-dsvector-jsonserialize-function/](https://www.geeksforgeeks.org/php-dsvector-jsonserialize-function/)

**ds\Vector：：jsonSerialize()**函数是 PHP 中的一个内置函数，用于返回可以转换为 JSON 的元素。

**语法：**

```php
*mixed* public JsonSerializable::jsonSerialize( void )

```

**参数：**此函数不接受任何参数。

**返回值：**此函数以可转换为 JSON 的形式返回向量值。

下面的程序说明了 PHP 中的**ds\Vector：：jsonSerialize()**函数：

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

echo("Elements after converting to JSON convertible form\n");

echo json_encode(new vector($arr), JSON_PRETTY_PRINT);

?>
```

发帖主题：Re：Колибри0.7.8.0

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
$arr = ["geeks", "for", "geeks"];

echo("Elements after converting to JSON convertible form\n");

echo json_encode(new vector($arr), JSON_PRETTY_PRINT);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/ds-vector.jsonserialize.php](http://php.net/manual/en/ds-vector.jsonserialize.php)