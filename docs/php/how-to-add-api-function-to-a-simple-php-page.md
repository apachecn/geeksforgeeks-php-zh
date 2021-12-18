# 如何给一个简单的 PHP Page 添加 API 函数？

> 原文:[https://www . geesforgeks . org/how-add-API-function-to-a-simple-PHP-page/](https://www.geeksforgeeks.org/how-to-add-api-function-to-a-simple-php-page/)

**应用程序编程接口**是一个包含一组规则或协议或工具的系统，这些规则或协议或工具有助于通过标准数据访问在两个应用程序或软件之间提供交互。它非常类似于用于开发网页或移动应用程序的网络服务。一个应用程序可以调用其他程序的应用编程接口来利用一些功能。**应用编程接口**获取请求并在程序员的软件系统中返回结果。
如果系统与数据库通信，那么应用编程接口由 PHP 扩展公开。

**例子:**谷歌地图 API，youtube API。

**先决条件:**

1.  服务器端编程语言（Professional Hypertext Preprocessor 的缩写）
2.  PHP cURL 库

**程序:**

```php
<?php

$url = 'RequiredLink';
$data = [
    'collection'  => 'RequiredAPI'
];

$curl = curl_init($url);

function APIcall($method, $url, $data) {
    $curl = curl_init();

    switch ($method) {
        case "POST":
            curl_setopt($curl, CURLOPT_POST, 1);
            if ($data)
                curl_setopt($curl, CURLOPT_POSTFIELDS, $data);
            break;
        case "PUT":
            curl_setopt($curl, CURLOPT_CUSTOMREQUEST, "PUT");
            if ($data)
                curl_setopt($curl, CURLOPT_POSTFIELDS, $data);
            break;
    }

    curl_setopt($curl, CURLOPT_URL, $url);
    curl_setopt($curl, CURLOPT_HTTPHEADER, array(
        'APIKEY: RegisteredAPIkey',
        'Content-Type: application/json',
    ));

    curl_setopt($curl, CURLOPT_RETURNTRANSFER, 1);
    curl_setopt($curl, CURLOPT_HTTPAUTH, CURLAUTH_BASIC);
    $result = curl_exec($curl);

    if(!$result) {
        echo("Connection failure!");
    }
    curl_close($curl);
    return $result;
}
?>
```

**网络应用程序接口的类型:**网络应用程序接口是那些可通过互联网访问的接口。

1.  **开放 API:**这些 API 是公开的，因为没有限制。
2.  **合作伙伴 API:**用户需要许可证和特殊权限才能访问这类 API。
3.  **私有 API:**内部系统公司所有。
4.  **复合 API:**它是数据和服务 API 的组合，用于加快执行过程。

除了以上四个之外，还有很多其他的 API。有些 API 可以在网上找到，你不需要安装软件。

**Web Service API 的类型:**一个非常常见的例子，使用支付流程 API 而不是开发我们自己的支付流程。Web 服务 API 是通过网络连接访问的独立于平台的方法。

1.  **SOAP:** 简单对象访问协议，使用 web 服务定义语言或 XML 进行数据传输。它非常健壮。这些用于集成应用编程接口。
2.  **JSON-RPC:** 数据传输使用 JSON。
3.  **REST:** The set of rules includes some standard architectural principals for data exchange. For making a request, it uses HTTP methods of getting, PUT, POST, PATCH, DELETE for all CRUD operations. It consumes less bandwidths and also comfortable accessing cloud services.

    **REST 输出为 JSON 的形式:**

    *   **获取:**读取或检索信息。
    *   **开机自检:**创建新记录。
    *   **PUT:** 更新一条记录。
    *   **删除:**删除记录。

每当应用程序使用所有四种数据库操作进行创建、读取、更新和删除时。据说它使用了 REST 应用编程接口。并非所有的应用编程接口都是网络服务，但所有的网络服务都是应用编程接口。一个非常常见的例子是 REST APIs。REST APIs 是互联网和网络服务的支柱。

**。htaccess** 文件用于将请求 URI 映射到 REST API 服务。

```php
<?php
require_once("MobileRestHandler.php");

$mobileRestHandler = new MobileRestHandler();
$mobileRestHandler->getAllMobiles();
?>
```

*   **GET:** 获取信息或收集数据。例如，表中的产品详细信息。

    > $ return data = callAPI(' GET '，' https://API . geeksforgeeks . com/URL _ for _ GET/' .$user['user']['buyer_id']，false)；
    > $ response = JSON _ decode($ return data，true)；
    > $ errors = $ response[' response '][' errors ']；
    > $ data = $ response[' response '][' data '][0]；

*   **POST:** 添加或创建新信息，如某餐厅的反馈或评论。

    > $ arrayOfData = array(
    > )买方" =>$ user[' user '][' buyer _ id ']，
    > "付款" = >阵列(
    > "账号" =>$本- >请求- >数据['账号】、
    > ”路由" =>$本- >请求- >数据['路由】、
    > ”方法" =>$ this->
    > $ apiCall = apiCall(' POST '，' https://API。极客们。com/URL _ for _ POST/'，JSON _ encode($ data _ array))；
    > $ response = JSON _ decode($ apiCall，true)；
    > $ errors = $ response[' response '][' errors ']；
    > $ data = $ response[' response '][' data '][0]；

*   **PUT:** 更新现有数据。

    > $ arrayOfData = array(
    > )金额" = >"要求安装"
    > )；
    > $updateData = APIcall('PUT '，' https://API。极客们。com/URL _ for _ PUT/'。$ putParameter，
    > JSON _ encode($ Arrayofdata))；
    > $ response = JSON _ decode($ updateData，true)；
    > $ errors = $ response[' response '][' errors ']；
    > $ data = $ response[' response '][' data '][0]；

*   **删除:**删除现有数据。

    > APIcall('DELETE '，' https://API。极客们。com/URL _ for _ DELETE/' .$required_id，false)；

**用 PHP cURL 使用 API:**

*   **获取 API 密钥:**当你开始使用 API 时，你应该注册并获取一个密钥，它是一串字母和数字。此应用编程接口密钥仅在发出请求时使用，以便服务器应用编程接口将用户识别为注册用户。
*   **用 PHP 应用程序测试 API:**这个过程检查一切是否如预期的那样工作。
*   使用 API 开发所需的 PHP 应用程序。使用必要的 API 创建或开发应用程序。

**创建 REST API 的步骤:**

1.  创建数据库和数据库表。
2.  建立数据库连接。
3.  创建一个 REST API 文件。
    *   创建索引或 HTML 文件。
    *   通过 cURL 从数据库中获取记录