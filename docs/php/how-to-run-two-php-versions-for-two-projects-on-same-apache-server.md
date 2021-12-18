# 如何在同一个 apache 服务器上为两个项目运行两个 PHP 版本？

> 原文:[https://www . geesforgeks . org/how-to-run-two-PHP-versions-for-two-project-on-同一个 apache-server/](https://www.geeksforgeeks.org/how-to-run-two-php-versions-for-two-projects-on-same-apache-server/)

在本文中，我们将学习在同一个 Apache 服务器上运行两个版本的 PHP。为了管理多个域，Apache 网络服务器在单个实例上使用虚拟主机。

**先决条件:**我们将使用 XAMPP 服务器来使用 Apache 服务器，并掌握一些使用它的知识。

首先，下载旧版本的 XAMPP，可以是任何版本。旧版本是 XAMPP 1.8.2，后来我们安装了最新版本的 XAMPP。XAMPP 的两个版本将拥有相同的 apache 服务器。

**步骤:**

1.  下载 xampp-win32-1.8.2-6-VC9-Installer.exe

    ![](img/47fe5a6683a20a92d7ccf74483dc7aa0.png)

2.  安装软件。

    ![](img/f481b49942524919885c44d2dddf940a.png)

3.  点击下一步。

    ![](img/16554fc4a2fc8ba22841237c14725b63.png)

4.  更改名称(最好使用 XAMPP_1_8_2)，以便以后您能够区分新版本和旧版本。

    ![](img/40df87ff37b49cc7936e5ed61abf6d9a.png)

5.  点击“安装”完成安装过程。

    ![](img/be58f686acd1cd339645bb2a4777b23a.png)

    ![](img/0e48165fd6a57f07ca76b57b2dfd872f.png)

*   打开保存 XAMPP1_8_2 的文件夹位置。
    ![](img/58b0375759331389d9edd16dc58a8712.png)
*   点击 XAMPP _ 1 _ 8 _ 2–>阿帕奇
    ![](img/33896d743cb4260423ad49610eb23bf8.png)

配置文件 httpd CONF 文件以更改新 XAMPP 的端口。由于两个不同版本的 XAMPP 不能在同一个端口上运行，我们需要切换到该端口。

**改变 XAMPP1_8_2 端口的步骤:**

打开文件 HTTP CONF 文件>将端口从 80 更改为 8080。

![](img/d238454754b51aff99b9e27c375e763e.png)

*   更改端口后，单击保存并退出。
*   现在转到额外的文件夹
*   要在 ssl CONF 文件中进行的更改
*   将听音 443 改为 444

![](img/ea2ed01733ded9b79376a949675323f0.png)

![](img/2a96c3ee8ac5dce5ea2ef59687afb38b.png)
![](img/828065bc978d69b7f1ee977b331c47c7.png)

*   全部保存并退出。
*   现在下载 XAMPP 新版本
*   遵循相同的步骤{1、2、3、4、5、6}
*   不要改变任何东西，比如港口。
*   打开 XAMPP1_8_2 控件
*   打开 XAMPP 新版本控制。

![](img/cac5c4ffbbbdc3edfbe5e2c7ad9dd739.png)
![](img/8d7ed9f0cedcd34bae1ae233878fb779.png)

**注意:**你可能会遇到 3306 端口的一些问题。

![](img/5af490948249bbf7841ad31bc5a87c16.png)

将端口 3306 更改为 3307

**更换端口的步骤:**

*   在“my.ini”文件中更改 MySQL 的配置文件。

    ![](img/d93c70d15fcc8803988bf28689931dd0.png)

*   将端口更改为 3307

    ![](img/82c902617befc826ca913c6def199187.png)

*   运行代码:

    ## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

    ```
    <?php
        phpinfo();
    ?>
    ```

*   将上述代码保存在新版本和旧版本的 XAMPP 文件夹的“htdocs”文件夹中。

    ![](img/be23db21ef6b6645cf44f43866d3fb81.png)

*   保存在 XAMPP 文件夹的“htdocs”文件夹中。

    ![](img/2fe3590a5745e67faf1ef041f7c4c22e.png)

*   XAMPP_1_8_2 也是如此

    现在，打开浏览器，然后键入命令。

    ```
    localhost/phpinfo.php
    ```

    ![](img/8317d31d4aaf303c5d78afdfcfff50fb.png)
    **输出:**
    ![](img/52ab7b442106f696fce4e2a02bd16ed2.png)

    这是一个版本 **7.4.2** 。

    现在对于第二个版本，键入命令。

    ```
    localhost:8080/phpinfo.php
    ```

    **输出:**
    ![](img/dc598a370abad1a7e5e4615cb8071c11.png)

    最后，我们能够在同一个 Apache 服务器上执行两个 PHP 版本(7.4.2 和 5.4.27)。