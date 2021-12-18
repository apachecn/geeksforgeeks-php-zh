# PHP 7.4 新特性

> 原文:[https://www.geeksforgeeks.org/new-features-of-php-7-4/](https://www.geeksforgeeks.org/new-features-of-php-7-4/)

**简介:** PHP 是一种流行的通用脚本语言。它用于网络开发。它是由拉斯马斯·勒德尔夫在 1994 年创建的，PHP 参考实现现在由 PHP 集团生产。

**PHP 7.4 更新 2019:** 时不时的新特性对于任何语言的成长都是非常必要和重要的。PHP 是多年来流行的语言之一，其中一个主要原因是他们不断更新它，并不时向它添加新功能。PHP 从最初发布到现在的性能都要好得多。此外，PHP 是十大最受欢迎的编程语言之一。

**新特性:**PHP 7.4 的一些新特性如下:

**1。数组中的扩展运算符:** PHP 7.4 将赋予在数组中使用扩展运算符的权力，这比 array_merge 更快。扩展运算符被认为是一种语言结构，array_merge 是一个函数。此外，编译时也得到了优化。

**示例:**这些是添加的新功能及其工作原理的图示。

```php
$prime = ['2', '5'];
$all = ['1', '3', ...$prime, '7'];
```

**输出:**

```php
1, 3, 2, 5, 7
```

**2。弱引用:**在 PHP 7.4 中，WeakReference 类允许我们保存到对象的链接。它不像 weakerf 扩展的 weakerf 类。由于这个特性，我们可以很容易地实现类似缓存的结构。

```php
<?php
class Cache {

    // var WeakReference[]
    private $objects = [];

    // $id is an identifier to store
    // the object, int|string

    // Return the stored object,
    // or null if that object is
    // not in the cache
    public function getObject($id) {
        $reference = $this->objects[$id] ?? null;

        if($reference === null){
            return null;
        }

        return $reference->get();
    }

    // The $id is the identifier for
    // the stored object, int|string
    // $object is used to store the object
    public function setObject($id, $object) {
        $this->objects[$id] = 
            WeakReference::create($object);
    }
}
?>
```

上面的代码是弱引用的一个例子。弱引用类似于普通引用，只是它不阻止垃圾收集器收集对象。
**WeakReference** 不应该和 **WeakRef** 混淆，后者是一个 PHP 扩展，不是 PHP 的原生部分。

**3。预加载:**这个功能我们可以在 OPcache 中上传文件、库。这些功能使我们能够将文件预加载到内存中。

**示例:**只是一个伪实现。

```php
$files = /* An array of files 
    that you want to preload */;

foreach ($files as $file) {
    opcache_compile_file($file);
}
```

您想要预加载的每个 PHP 文件都应该被传递给 opcache_compile_file()或者从预加载脚本中被要求一次。

**4。箭头函数:**它消除了之前的复杂性，因为使用匿名函数增加了 PHP 的复杂性。现在，这些特性允许我们使我们的代码更加简洁，并对其进行清理。这只是为了消除复杂性并简化代码。

```php
// A collection of Post objects
$posts = [/* … */];

$ids = array_map(function ($post) {
    return $post->id;
}, $posts);
```

在更新之前，我们必须编写上面提到的代码。

```php
// A collection of Post objects
$posts = [/* … */];

$ids = array_map(fn($post) => $post->id, $posts);
```

*   它们以关键字 **fn** 开始
*   它们只有一个表达式，那就是 return 语句
*   不允许使用 return 关键字

**5。从 __toString()函数抛出异常:**以前，用于将对象转换为字符串的函数存在于标准库中，并且其中许多函数没有正确处理异常。

**语法:**

```php
public Exception::__toString( void ) : string
```

**返回值:**是异常的字符串表示。

```php
<?php
try {
    throw new Exception("error");
} catch(Exception $e) {
    echo $e;
}
?>
```

**6。合并赋值运算符:**当我们必须将三元运算符与 **isset()函数**一起使用时，这非常有用。这使您能够返回第一个操作数(如果存在)，否则将返回第二个操作数。PHP 7 中引入了空合并相等运算符，以简化使用三元运算符的 isset()检查。

```php
// Before the 7.4 release
$data['username'] = $data['username'] ?? 'guest';

// After 7.4 new feature
$data['username'] ??= 'guest';
```

**7。数字文字分隔符:**数字文字可以在数字之间包含下划线。

```php
6.674_083e-11; // float
299_792_458;   // decimal
0xCAFE_F00D;   // hexadecimal
0b0101_1111;   // binary
```

**Filter:**Filter _ VALIDATE _ FLOAT 过滤器支持 min_range 和 max_range 选项，语义与 FILTER_VALIDATE_INT 相同。

**FFI:** FFI 是一个新的扩展，它是调用本机函数、访问本机变量以及创建/访问 C 库中定义的数据结构的简单方法。

**GD:** 添加了 IMG _ 过滤器 _ 散射图像过滤器，用于对图像应用散射过滤器。

**Hash:** 使用 Castagnoli 多项式添加了 crc32c hash。该 CRC32 变体用于存储系统，如 iSCSI、SCTP、Btrfs 和 ext4。

**PDO:** 用户名和密码可以指定为 mysql、mssql、sybase、dblib、firebird 和 oci 驱动程序的 PDO DSN 的一部分。在 php 7.4 发布之前，这个特性只被 pgsql 驱动程序支持。

**参考:**T2】https://www.php.net/manual/en/migration74.new-features.php