# PHP|预定义的类和接口

> Original: [https://www.geeksforgeeks.org/php-predefined-classes-and-interfaces/](https://www.geeksforgeeks.org/php-predefined-classes-and-interfaces/)

有[类](https://www.geeksforgeeks.org/php-classes/)和[接口](https://www.geeksforgeeks.org/php-interface/)可以是用户定义的，也可以是 PHP 语言预定义的。

PHP 中有 9 个预定义的类和接口：

*   可穿越
*   迭代器
*   迭代器聚合
*   投掷桌
*   ArrayAccess
*   可系列化
*   关闭 / 封锁 / 辩论终止提付表决 / 解脱
*   发电机

**Traversable：**Traversable 接口中没有方法，仅充当其他预定义的 Traversable 类的基础。 通过使用 foreach 构造和此接口，可以很容易地检测到类是否可遍历。

**迭代器：**这是一个预定义的接口，用于能够内部迭代自身的对象或外部迭代器。 此接口扩展了 Traversable 接口。 该接口的五个方法分别是：

<figure class="table">

| Method name | Parameters | Return value | Description |
| --- | --- | --- | --- |
| 目前的 / 通用的 / 流通的 / 最近的 | 无效的 / 空的 / 空无所有的 / 缺门的 | 混合的 / 搀和的 / 形形色色的 / 弄糊涂的 | Returns the present value. |
| 钥匙 / 键 / 关键 / 主调 | 无效的 / 空的 / 空无所有的 / 缺门的 | Scalar quantity | Returns the key of the current value. |
| Next one | 无效的 / 空的 / 空无所有的 / 缺门的 | 无效的 / 空的 / 空无所有的 / 缺门的 | Move on to the next element. |
| 倒带装置 / 重绕 / 倒带器 | 无效的 / 空的 / 空无所有的 / 缺门的 | 无效的 / 空的 / 空无所有的 / 缺门的 | 将文件指针的位置设置为文件的开头。

 |
| 有效的 / 确凿的 / 令人信服的 / 具有法律效力的 | 无效的 / 空的 / 空无所有的 / 缺门的 | 布尔尔 | Check to see if the array contains more entries. |

</figure>

**IteratorAggregate：**此接口是 Traversable 接口的扩展，只有一个方法。

<figure class="table">

| Method name | Parameters | Return type | Description |
| --- | --- | --- | --- |
| GeTiterator GetIterator | 无效的 / 空的 / 空无所有的 / 缺门的 | 可遍历 | This function is used to retrieve iterators (external). |

</figure>

#### 投掷桌

此功能在 PHP 版本 7 中可用。所有通过 Throw 语句抛出的对象都有一个接口，该接口充当称为 Throwtable 的基接口。 Exception 和 Error 类使用此接口。

<figure class="table">。

| Method name | Number of parameters | Parameter name | Return type | Description |
| --- | --- | --- | --- | --- |
| 获取消息 | 0 | 无效的 / 空的 / 空无所有的 / 缺门的 | 线 / 细绳 / 一连串 / 纤维 | 获取消息 | 0 | 无效的 / 空的 / 空无所有的 / 缺门的 | 细绳 |
| 获取精度 | 0 | 无效的 / 空的 / 空无所有的 / 缺门的 | Thwtable | The previous exception was returned. |
| GetCode： | 0 | 无效的 / 空的 / 空无所有的 / 缺门的 | 混合的 / 搀和的 / 形形色色的 / 弄糊涂的 | The generated exception code. |
| GetFile | 0 | 无效的 / 空的 / 空无所有的 / 缺门的 | 细绳 | Returns the file where the exception occurred. |
| GetLine | 0 | 无效的 / 空的 / 空无所有的 / 缺门的 | 集成 | Returns the line number where the exception occurred. |
| 获取跟踪 | 0 | 无效的 / 空的 / 空无所有的 / 缺门的 | 有序的安排 / 排列 / 大批 | Return to the stack trace. |
| GetTraceAsString | 0 | 无效的 / 空的 / 空无所有的 / 缺门的 | 细绳 | The stack trace is returned as a string. |
| __toString | 0 | 无效的 / 空的 / 空无所有的 / 缺门的 | 细绳 | The generated exception is returned as a string. |

</figure>

**ArrayAccess：**此接口允许将对象作为数组进行访问。 它有 4 个方法：

<figure class="table">

| Method name | Parameters | Return | 描述 / 描写 / 形容 / 类别 |
| --- | --- | --- | --- |
| OffsetExists | OffsetValue(混合) | 布尔尔 | Check to see if there is an offset. |
| 偏移获取 | Offset value (blend) | Mix | The offset is retrieved by this method. |
| 偏移量 | Offset value (blend), element (blend) | 无效的 / 空的 / 空无所有的 / 缺门的 | The above offset is assigned some values. |
| 偏移未设置 | Offset value (blend) | 无效的 / 空的 / 空无所有的 / 缺门的 | The offset value is not set. |

</figure>

**Serializable：**这个类允许以定制的方式进行序列化。 如果需要序列化实例，则调用 Serialize()方法。 如果它是在某个方法内部的代码中编写的，则不会对程序产生任何更改或副作用。 该接口有两个方法：

<figure class="table">

| Method name | Parameters | 回 / 返回 / 归还 / 产生 | 描述 / 描写 / 形容 / 类别 |
| --- | --- | --- | --- |
| 连载 / 连续播出 / 使连续 | 无效的 / 空的 / 空无所有的 / 缺门的 | 细绳 | Object to a string. |
| De-serialization | Serialize string (string) | 无效的 / 空的 / 空无所有的 / 缺门的 | Objects that are converted to strings are converted back to objects. |

</figure>

**闭包：**PHP 中有一些称为匿名函数的函数没有名称。 回调参数被赋值为匿名函数。 有 5 种方法：

<figure class="table">

| Method name | Parameters | Return | Description |
| --- | --- | --- | --- |
| __ 构造 | 无效的 / 空的 / 空无所有的 / 缺门的 | 无效的 / 空的 / 空无所有的 / 缺门的 | Constructor does not allow instantiation | . Binding | 对象(闭包)newthis(对象)闭包 | Closure | Closures can be copied by the class scope and the specific binding objects mentioned. |
| 绑定 | Newthis (object) closure | Closure | Closures can be copied by class scope and newly bound objects. |
| Call | Newthis (object) closure | Mix | Bind and invoke the closure. |
| From a callable object | Callable (callable) | Closure | Callable objects are converted to closures. |

</figure>

**Generator：**此接口是迭代器的扩展，有 9 个方法：

<figure class="table">

| Method name | Parameters | Return | Descending order |
| --- | --- | --- | --- |
| 目前的 / 通用的 / 流通的 / 最近的 | 目前的 / 通用的 / 流通的 / 最近的 | 目前的 / 通用的 / 流通的 / 最近的 | And MIXED [T23. |
| 获取返回值 | 无效的 / 空的 / 空无所有的 / 缺门的 | Or MIXED | Function returns the value of the generator. |
| 钥匙 / 键 / 关键 / 主调 | Invalid | Or mix | Returns the resulting key. |
| Next one | Invalid | Invalid | . |
| Rewind | Rewind | Rewind | . |
| Send | Value (mixed) | Or mix | If the value is sent to the generator. |
| Throw out | Exception (can be thrown) | Mix | If the exception is thrown into the generator. |
| 有效的 / 确凿的 / 令人信服的 / 具有法律效力的 | 无效的 / 空的 / 空无所有的 / 缺门的 | 布尔尔 | Verify that the iterator is off. |
| __WAKUP | 包含 | 包含 | The callback is serialized. |

</figure>