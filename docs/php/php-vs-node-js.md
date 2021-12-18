# PHP 与 Node.js

> Original: [https://www.geeksforgeeks.org/php-vs-node-js/](https://www.geeksforgeeks.org/php-vs-node-js/)

[PHP](https://www.geeksforgeeks.org/php-introduction/)和 Node.js 都用于服务器端开发，因此成为彼此的竞争对手。 下面是基于不同参数的一些不同之处，以理解这两个巨头之间的差异并做出决定。

### [PHP](https://www.geeksforgeeks.org/php-introduction/)vs Node.js

| PHP | Node.js |
| --- | --- |
| [PHP](https://www.geeksforgeeks.org/php-introduction/)是 Rasmus Lerdorf 于 1994 年创建的**超文本预处理器**的首字母缩写。 [PHP](https://www.geeksforgeeks.org/php-introduction/)是专门为 Web 开发设计的开源服务器端脚本语言。 虽然[PHP](https://www.geeksforgeeks.org/php-introduction/)是一种服务器端脚本语言，但它也被用作通用脚本语言。 [PHP](https://www.geeksforgeeks.org/php-introduction/)脚本的扩展名为**.php**，可以包含[Javascript](https://www.geeksforgeeks.org/javascript-tutorial/)、[HTML](https://www.geeksforgeeks.org/html-basics/)、[CSS](https://www.geeksforgeeks.org/css-introduction/)，甚至可以包含纯文本。 | Js 是基于[Chrome 的 JavaScript Engine(V8)](https://developers.google.com/v8/)构建的开源服务器端[Javascript](https://www.geeksforgeeks.org/javascript-tutorial/)运行时环境。 Js 用于构建快速且可伸缩的应用程序，是一种事件驱动的非阻塞 I/O 模型。 Node.js 文件的扩展名为**.js**，仅包含[Javascript](https://www.geeksforgeeks.org/javascript-tutorial/)。 它的原著作者是 Ryan Dahl，最初于 2009 年 5 月 27 日发布。 随着 Node.js 的诞生，它为用户提供了构建完全基于[Javascript](https://www.geeksforgeeks.org/javascript-tutorial/)的应用程序的功能。 |

### 语法和对命令行的访问

两个平台都可以通过以下方式访问命令行界面：

| PHP | Node.js |
| --- | --- |
| $php-i | $NODE |

**示例：**用 PHP 和 Node.js 打印‘Hello World’
以下代码段比较了用这两种语言打印‘Hello World’程序：

## PHP

```php
// Printing Hello GeeksforGeeks in PHP
echo 'Hello GeeksForGeeks';   
```

## Node.js

```php
console.log('Hello GeeksForGeeks');
```

**注意：**要运行 Node.js 代码，请使用[REPL](https://www.geeksforgeeks.org/node-js-repl-read-eval-print-loop/)环境。

### 同步或异步

**同步代码**逐行执行，并在当前行执行完后继续执行下一行代码。
**异步代码**同时执行所有代码。

| PHP | Node.js |
| --- | --- |
| [PHP](https://www.geeksforgeeks.org/php-introduction/)是同步的，但是有些 API 的行为与同步批次不同。 同步的问题可以通过一个简单的例子来理解。 假设第一行代码有一个需要花费大量时间执行的函数。 现在，由于同步的性质，下面的代码行必须等待轮到它们，并且只有在函数执行之后才会执行。 这会使速度变慢，用户需要等待。 | Js 本质上是异步的，这意味着 JavaScript 引擎一次性运行整个代码，而不是等待函数返回。 函数下面的代码行将执行，函数也将执行，一旦执行完毕将返回输出，从而使 Node.js 变得更快。 |

**注意：**如果许多函数需要链接，这可能需要通过管道将数据从一个函数传递到另一个函数，程序可能会陷入“回调地狱”。 但是，它可以由 Node.js 解决，因为它具有[异步/等待](https://www.geeksforgeeks.org/using-async-await-in-node-js/)特性，可以帮助代码块同步执行。

### 上下文切换

不同环境和语言之间的切换归因于编写代码时效率的下降。 在多种编码语言之间切换会降低程序员的效率。

| PHP | Node.js |
| --- | --- |
| 用[PHP](https://www.geeksforgeeks.org/php-introduction/)编写后端代码，用户不断地在不同的语言和语法之间切换。 这是因为[PHP](https://www.geeksforgeeks.org/php-introduction/)主要用作[LAMP](https://www.geeksforgeeks.org/installing-php-and-configuring-it-on-ubuntu-14-04-trusty/)堆栈的一部分，该堆栈包括 MySQL(用于数据库)、[PHP](https://www.geeksforgeeks.org/php-introduction/)(用于服务器端代码)和 Linux。 它们都有不同的语法，并且需要对 HTML、CSS 和[Javascript](https://www.geeksforgeeks.org/javascript-tutorial/)有很好的了解。 | 因为 Node.js 是用 JavaScript 编写的，所以两端都是基于 JavaScript 的服务器端和客户端，因此不需要在语言之间切换。 [Javascript](https://www.geeksforgeeks.org/javascript-tutorial/)栈(Mean 或 MERN)更好，因为使用的唯一编码语言和语法是基于[Javascript](https://www.geeksforgeeks.org/javascript-tutorial/)的。 |

### 模块

| PHP | Node.js |
| --- | --- |
| [PHP](https://www.geeksforgeeks.org/php-introduction/)使用模块安装技术，如 PEAR(一个经验丰富的软件包系统)和相对较新的 Composer。

*   [PEAR](https://pear.php.net/) is a framework and distribution system for reusable PHP components.
*   [Composer](https://getcomposer.org/doc/00-intro.md) is a dependency management tool in PHP. It allows the user to declare the libraries on which the project depends and will manage (install / update) these libraries for the user.

 | **Node.js**捆绑了一个名为[npm(Node Package Manager)](https://www.geeksforgeeks.org/node-js-npm-node-package-manager/)的包管理系统及其注册表，该注册表易于使用和发布。 |

### 框架

| PHP | Node.js |
| --- | --- |
| [PHP](https://www.geeksforgeeks.org/php-introduction/)是一种非常流行的服务器端脚本语言，它有许多框架可以帮助您轻松地进行后端开发。 其中一些框架是[Laravel](https://laravel.com/)、[CodeIgniter](https://ellislab.com/codeigniter/)、[Cakephp](https://cakephp.org/)等。这些框架有助于敏捷、健壮和安全的 Web 应用后端开发。 | 像[Express](http://expressjs.com)和全栈 MVC 框架[Meteor](http://www.meteor.com)和[Derby](http://derbyjs.com)这样的框架最受欢迎。 新的框架不断涌现，比如**koa.js**、**Hapi**、**total.js**、**sails.js**等。 |

**示例：**Laravel 框架

```php
// requires Composer installed on your system
// run following command on terminal.
// This installs laravel on your system
composer global require "laravel/installer"

// Below command creates a folder called
// GeeksForGeeks with laravel installed
laravel new GeeksForGeeks

```

**示例：**Express Framework Web 服务器：

```php
// Below command installs ExpressJS 
// in your project folder
npm install express --save

// creating web server using Express framework
// write the following code in your gfg.js file

var express = require('express');
var app = express();
express.listen('3000', function(){
console.log(' GeeksForGeeks demo server
                  running on express');
});

```

### 数据库

| PHP | Node.js |
| --- | --- |
| [PHP](https://www.geeksforgeeks.org/php-introduction/)与 MySQL、MariaDB、PostgreSQL 等传统/关系数据库协作使用。然而，也有一些方法可以将 NoSQL 数据库系统与[PHP](https://www.geeksforgeeks.org/php-introduction/)一起使用，但它们不是很流行。 | **Node.js**与 NoSQL(不仅仅是 SQL)数据库(如 MongoDB、CouchDB)和图形数据库系统(如 Neo4j)完美配合。 几乎所有数据库的 NPM 包都可以在 NPM 注册表中找到。 |

**负点 PHP：**MySQL 数据库系统特别容易受到 SQL 注入攻击、交叉脚本(XSS)等攻击。

**负点 Node.js：**尽管 NoSQL 注入攻击并不常见，但它是一个有记录的漏洞。 但与 SQL 注入相比，它们微不足道。 这主要是因为它们是新的，并且它们的代码设计方式是这样的，即它们天生就能抵抗这类攻击。

### Web 服务器

| PHP | Node.js |
| --- | --- |
| 对于 5.4 之前的版本，必须安装 LAMP 和 XAMPP(**Cross**-Platform，**A**PACHE，**M**ariaDB，**P**HP)服务器。
但是从 V5.4 开始，[PHP](https://www.geeksforgeeks.org/php-introduction/)附带了一个可以使用的内置开发服务器。 | **NodeJS**是为网络应用开发的。 它附带了一些核心模块，如 http、DNS、文件系统等，可以帮助开发定制的 Web 服务器。 支持运行 Web 服务器的 Node.js 的一些非常流行的框架是 Express.js、koa.js 和 Sails.js，它们最多只需使用 4 行代码即可设置。 |

**示例：**启动 PHP 服务器

```php
// starting php server
$ php -S localhost:8000

// index.js file code
<?php
  echo 'Hello! This is GeeksForGeeks';
?>
```

提供[PHP](https://www.geeksforgeeks.org/php-introduction/)Web 服务器是为了帮助应用程序开发，因此不能作为成熟的 Web 服务器有效使用。

**示例：**启动 Node.js 服务器

```php
// starting Node.js server
$ node app.js

    // app.js source code
    var http
    = require('http');
http.createServer(function(req, res) {
        res.writeHead(200, { 'Content-Type' : 'text/plain' });
        res.end('Hi Programmer\n');
    })
    .listen(8080, '127.0.0.1');
console.log('GeeksForGeeks Server running at http://127.0.0.1:8080/');
```

自己的 Web 服务器可以用 Node.js 编码，Node.js 应用程序可以在其上运行。 如果配置和监控得当，这些服务器具有高可伸缩性的潜力。

### 应用程序域

| PHP | Node.js |
| --- | --- |
| 

*   Used to develop CPU-intensive applications, such as weather applications and science applications.
*   The LAMP stack is used for API development.
*   CMS (content management system) is the same as WordPress, Drupal also uses [PHP](https://www.geeksforgeeks.org/php-introduction/) , which makes it possible to create blogs, websites, e-commerce sites, and so on.

 | 

*   NodeJS is ideal for developing highly scalable server-side solutions because of its non-blocking Icano and event-driven model.
*   It is widely used in chat applications, blogs, video streaming applications and other real-time applications.
*   Used to develop single-page applications, such as resume folders and personal websites.

 |

**注意：客户端不需要与服务器反复交互的应用应该使用**[PHP](https://www.geeksforgeeks.org/php-introduction/)，客户端和服务器之间需要大量交互的应用应该使用 Node.js。