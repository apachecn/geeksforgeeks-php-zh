# Laravel |前端脚手架

> 原文:[https://www . geesforgeks . org/laravel-前端-脚手架/](https://www.geeksforgeeks.org/laravel-front-end-scaffolding/)

前端支架意味着为应用程序创建一个基本结构。Laravel 提供了一种非常简单的方法，可以使用任何其他可用的支架(如 **Bootstrap** 、 **Vue** 和 **React** )来更改前端预设/支架。

**生成脚手架:**

*   **Step 1:** To generate a scaffolding, we first need to install the **laravel/ui**, which is a **composer** package and to do that we have to run the following composer command.

    ```php
    composer require laravel/ui --dev
    ```

    ![](img/bc72b20c1e2847ff8e70c49934c40215.png)

*   **Step 2:** After that, we can run the **ui** artisan command to generate a base scaffolding. As we discussed before, we can generate the scaffolding for Bootstrap, Vue or React and for that we will run the following artisan command.
    *   **自举**T0】
    *   **视图**

        ```php
        php artisan ui vue
        ```

    *   **反应过来**T0】

    ![](img/67b2958809bb8d70b6083faa268735d3.png)

    这将在**资源/js** 目录中创建一个**组件**目录。

    ![](img/2124d7f4300c7acacb32b083de8d5699.png)

*   **Step 3:** After running any of the above preset commands, we will have to install the npm, if it is not installed, to install run the following command.

    ```php
    npm install
    ```

    ![](img/d798431d8a094e6db0e6f85c25a3a47f.png)

*   **Step 4:** Now we have to run the following **npm** command to compile the scaffolding.

    ```php
    npm run dev
    ```

    ![](img/ade6cc0b4f7dc9bfae3cfe2a384e29de.png)

**通过身份验证生成支架:**必须完成生成支架步骤 1，然后按照以下步骤操作。

*   **step 1:** To generate a scaffolding with view files for authentication like login and register, then we just have to add ‘**–auth**’ at the end of the commands that we saw previously, as follows:
    *   **自举**T0】
    *   **视图**

        ```php
        php artisan ui vue --auth
        ```

    *   **反应过来**T0】

    ![](img/9ec4f293f4c2582067175050eb04b22b.png)

    这将在**资源/js** 目录中创建**组件**目录，并在**资源/视图**目录中创建带有**home.blade.php**文件的**授权**和**布局**目录。

    ![](img/e0eb7635506c50461e95fdf4077ecdee.png)

    *   **Step 2:** After running any of the above preset commands, we will have to install the npm if it is not installed, to install run the following command.

    ```php
    npm install
    ```

    ![](img/0f1eff19706233c1361636569bef7a89.png)

    *   **Step 3:** Now we have to run the following npm command to compile the scaffolding.

    ```php
    npm run dev
    ```

    ![](img/0e7b7b0fbdb73ad50e4599f6fe334cff.png)

    **移除脚手架:**要移除生成的脚手架，我们将运行以下 artisan 命令。

    ```php
    php artisan preset none
    ```

    ![](img/6adcb244e306b637545f2c8ecd1e77c7.png)

    **注意:**这将删除**组件**目录，该目录已创建，但不会删除**资源/视图**目录中在**验证**支架期间创建的文件和目录。

    **参考:**T2】https://laravel.com/docs/6.x/frontend