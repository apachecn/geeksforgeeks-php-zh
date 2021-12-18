# “PHP 工匠转储-自动加载”和“composer 转储-自动加载”的区别

> 原文:[https://www . geesforgeks . org/difference-PHP-artisan-dump-autoload-and-composer-dump-autoload/](https://www.geeksforgeeks.org/difference-between-php-artisan-dump-autoload-and-composer-dump-autoload/)

**PHP Artisan:** Artisan 是一个命令行 UI，可以在您构建应用程序时为您提供帮助。PHP artisan 命令在更短的时间内执行多个任务，效率更高。它可以用来创建模型、创建缓存、创建控制器，也可以用来创建 Laravel 包和添加虚拟数据。

**PHP 匠服:**这个命令可以用来运行你的应用程序。它也用于开发和测试目的。

*   默认情况下，它将主机名作为本地主机。

    ```
    php artisan serve
    ```

*   如果您想更改主机名和端口号，可以使用以下命令。

    ```
    php artisan serve --host=hostname.app --port=8080
    ```

**PHP artisan 命令的用法:**使用 Laravel 时需要知道的重要一点是，通过 localhost 运行你的项目是不可能的，它只能通过 **php artisan serve** 命令本身运行。

*   **创建模型:**该命令将生成模型**username.php**到预先存在的模型文件夹中，或者如果文件夹不存在，它将创建一个。您可以在此位置找到模型**app/Models/model name . PHP**

    ```
    php artisan make:model
    ```

*   **清除缓存:**当更多用户注册您的网站时，可能会导致认证系统失败， **[和](https://www.geeksforgeeks.org/laravel/)** 中的缓存可以使用这些命令清除。您也可以手动从存储中删除所有缓存文件和会话文件。
    *   刷新应用程序缓存

        ```
        php artisan cache:clear
        ```

    *   删除配置缓存文件

        ```
        php artisan config:clear
        ```

    *   清除所有已编译的视图文件

        ```
        php artisan view:clear 
        ```

*   **创建控制器:**以下命令用于创建控制器。
    在控制器文件夹内生成测试控制器

    ```
    php artisan make:controller TestController
    ```

**PHP 工匠转储-自动加载:****PHP 工匠转储-自动加载**命令调用带有优化标志的 Composer。它将**重新编译**加载的文件，创建巨大的**引导/编译. php**

**PHP Composer**Composer 是一个 PHP 编程语言的应用层包管理器。编辑器是一个管理 PHP 依赖关系的工具。在使用 composer 工具之前，您需要了解几个命令。

*   **Composer.json:** 要开始使用 Composer，您只需要一个 **composer.json** 文件。该文件包括您创建的项目的所有依赖项以及元数据。
    **作曲家**

    ```
    "autoload":{
        "classmap":["database"],
        "files":["name1.php", "name2.php"]
    },
    ```

*   **Composer install:**<srreong>Composer install</srreong>命令可用于添加依赖项。此命令不会更新任何内容。您需要手动将其添加到 **composer.json** 文件中，而如果 **composer.lock** 已经存在，请准确安装该文件中指定的内容，否则请读取 composer.json 文件以使其更容易。
*   **作曲家更新:****作曲家更新**命令可用于安装以及更新依赖项。该命令可用于添加或删除依赖项，但首先，手动添加到 **composer.json** 文件。
*   **Composer remove:** 此命令可用于移除未使用的依赖项。您可以使用下面的命令卸载这些依赖项。

    ```
    composer remove packageauthor/packagename
    ```

*   **Composer dump-autoload:****Composer dump-autoload**不会下载任何新的东西，它所做的只是再次寻找需要包含的所有类和文件。

**PHP artisan dump-autoload 与“PHP composer dump-autoload”的区别:**现在我们来简单了解一下 composer dump-autoload 和 PHP artisan dump-autoload 命令的区别。

| 作曲家转储-自动加载 | php artisan 转储-自动加载 |
| 它重新生成需要包含在项目中的所有类的列表(autoload_classmap.php)。 | 它将“重新编译”大量文件，创建巨大的 bootstrap/compiled.php |
| 它不会下载任何新的东西到项目中。 | 它会调用带有优化标志的作曲家。 |
| 找到所有工作台包和 composer dump-自动加载它们，一个接一个。 | 它将使用 composer 实现一些功能。 |
| 所有 Laravel 版本都支持该命令。 | 在 Laravel 5 和更高版本中不推荐使用此命令。 |