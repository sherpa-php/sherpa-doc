# Files tree

The **Sherpa** files tree was designed to be easy 
to use and encourage compliance with the MVC design pattern.

Thus, each element has its own location in files tree structure:

- ``src/`` : All your application files must be located in it
  - ``assets/`` 
    - ``medias/`` : Application images, videos, etc.
  - ``controllers/`` : Application controllers
  - ``core/`` : Internal framework files, **do not modify it!**
  - ``middlewares/`` : Application middlewares
  - ``models/`` : Application models
  - ``public/`` : Web server root with ``index.php`` main file
  - ``routes/`` : Routes repositories directory
  - ``views/`` : Application views
    - ``components/`` : Application views components

> **Sherpa** framework core uses the files tree directories and native files
> using original naming, please **do not edit them**.
{style="warning"}