# PHP 中 require-dev 和 require 的区别？

> 原文:[https://www . geesforgeks . org/require-dev 和 require-in-php 的区别/](https://www.geeksforgeeks.org/difference-between-require-dev-and-require-in-php/)

在了解*requires*和 requires _ dev 的区别之前，首先要了解 requires 和 requires _ dev 是什么。

> **要求:**这些是代码运行必须的包。它定义了实际的依赖关系以及包版本。
> **require_dev:** 它定义了开发项目所需的、生产环境中不需要的包。

**注意:**require 和 require_dev 是 **composer.json** 中可用的重要参数。

**什么是作曲家？**
Composer 是 php 中的依赖/参数管理器。它可以用来安装跟踪和更新项目依赖关系。Composer 还负责自动加载应用程序依赖的依赖项，让应用程序轻松地在项目中使用依赖项，而不用担心将它们包含在任何给定文件的顶部。项目的依赖项列在“composer.json”文件中，该文件通常位于项目根目录中。该文件保存有关生产和开发所需的软件包版本的信息。该文件可以使用任何文本编辑器手动编辑，也可以通过“composer require”或“composer require_dev”等命令通过命令行自动编辑。
要在项目中开始使用 composer 首先需要创建 composer.json 文件。它可以手动创建，也可以简单地运行 composer init。在终端运行 composer init 后，它会询问一些关于项目的基本信息，如包名、描述(可选)、作者和其他信息来源，如最低稳定性、许可证和所需的包。
composer . JSON 中的 *require* 键指定项目依赖于哪个包的 composer require 获取一个映射包名的对象
**示例:**

```
{
    "require": {

        // name of package.
        "composer/composer:" "1.2.*"
    }
}
```

在上面的示例中，“composer/composer”指定供应商名称和项目名称，用斜杠(“/”)和“1.2”分隔。* "指定版本名。
要安装依赖项，需要运行 composer install 命令，然后它会为所提供的版本约束找到该方法定义的包，并将其下载到供应商目录中。将第三方代码放入名为供应商的目录是惯例。installed 命令还创建了一个 composer.lock 文件。

**require 和 require_dev 之间的差异:**

*   **要求:**
    *   它定义了实际依赖性以及包版本。
    *   require 列出了此包所需的包。
    *   除非能够满足这些要求，否则不会安装软件包。
*   **require_dev:**
    *   它定义了开发项目所需的包。
    *   require_dev 列出了开发这个包或运行测试等所需的包。
    *   默认情况下，安装根包的开发需求。安装或更新都支持“–no-dev”选项，可防止安装 dev 依赖项。