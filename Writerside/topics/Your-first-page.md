# Your first page

> In order to create your first page properly, please make sure
> you have created a new project correctly.
> 
> Please read the following **Useful information** articles.
{style="warning"}

## Useful information

[📚 What is **MVC** pattern?](MVC-pattern.md)
: **Sherpa** uses MVC pattern in its structure. 
Let's learn what is MVC pattern before we start our first page!

[📚 How to create a new **Sherpa** project?](Installation.md)
: Let's create your first **Sherpa** project!

[📚 The **Sherpa** files structure](Sherpa-files-tree.md)
: Let's discover the **Sherpa** files tree!

## Tutorial introduction

To be original, our objective will be to display **Hello, World!**
on our first page.

**Let's follow the different steps!**

## Your first controller

We will learn to create our first **controller** class.
The **Sherpa** controllers use **PHP** back-end language
and extend the **Sherpa** native ``Controller`` class.

A controller can contain **static** and **dynamic** methods, 
but a **route method** we will discover later, must be
**dynamic**. 

**Here are the steps to create and prepare a new controller:**
- Go to ``src/controllers/`` directory.
- Create a new file named ``HelloController.php``.
- Copy and paste the following code into this file:
```PHP
<?php

namespace Sherpa\Template\controllers;

use Sherpa\Core\controllers\Controller;

class HomeController extends Controller
{

    public function helloWorld(): void
    {
        echo "Hello, World!";
    }

}
```

## Your first route

Your application's pages retrieving and usage are based
on **Sherpa** router system. This router is composed by
repository files. A first is created during project 
creation: ``main.php``. You can create as many repositories
you need, each one is loaded by **Sherpa** automatically.

> To prevent repositories **abusive loadings**, it is recommended
> to only create as many **as needed**.

**Here are the steps to create our first route:**
- Go to ``src/routes`` directory.
- Open ``main.php`` routes repository.
- Append to the current code the following line:
```PHP
Router::get("/hello", HelloController::class, "helloWorld");
```

> Please make sure you have imported all the **classes needed** 
> to create the route, like ``HelloController`` and ``Router`` classes.
{style="warning"}
