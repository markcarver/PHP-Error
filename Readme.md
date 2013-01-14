PHP Error
=========

PHP errors are not good enough for development, it's as simple as that. This aims to solve this.
This is the Drupal fork of the original library at https://github.com/JosephLenton/PHP-Error.

Getting Started
---------------

 * [Download the php\_error module](http://drupal.org/project/php_error)
 * Place it in the folder `/sites/all/modules` of your Drupal site.
 * [Download the php\_error library](https://raw.github.com/markcarver/PHP-Error/master/src/php_error.php), it's just one file.
 * Create the folder `php_error` in `/sites/all/libraries` and place the `php_error.php` library file in it (the full path should look like `/sites/all/libraries/php_error/php_error.php`).
 * Enable the PHP Error module at `/admin/modules`
 * Configure the PHP Error module at `/admin/config/development/php_error`

Features
--------
 * trivial to use, it's just one file
 * errors displayed in the browser for normal and ajaxy requests
 * ajax requests are paused, allowing you to automatically re-run them
 * makes errors as strict as possible (encourages code quality, and tends to improve performance)
 * code snippets across the whole stack trace
 * provides more information (such as full function signatures)
 * fixes some error messages which are just plain wrong
 * syntax highlighting
 * looks pretty!
 
 ![Better Error Message](http://i.imgur.com/1G77I.png)

 When an error strikes, the page is replaced with a full stack trace, syntax highlighting, and all displayed to be readable.

 ### Works with Ajax too!

 If the server errors during an ajax request, then the request is paused, and the error is displayed in the browser. You can then click to automatically retry the last request.

 ![ajax server stack trace](http://i.imgur.com/WRgug.png)

 This requires no changes to your JavaScript, and works with existing JS libraries such as jQuery.

 Check out the [project homepage](http://phperror.net) for a live demo.

Documentation
-------------

### [Example Setup](https://github.com/JosephLenton/PHP-Error/wiki/Example-Setup)

### [API](https://github.com/JosephLenton/PHP-Error/wiki/API)

### [Options](https://github.com/JosephLenton/PHP-Error/wiki/Options)

### [php.ini settings](https://github.com/JosephLenton/PHP-Error/wiki/php.ini)

Do not use on a live site!
--------------------------

This is intended for __development only__. It shows more about your site, gives you more info, and makes trivial errors fatal.
All of that is awesome if you want to debug quicker, and force high quality standards.

On a production server, that sucks, and is potentially unsafe.

In case you forget, you can disable this in production using the 'php_error.force_disabled' php.ini option (see below).

Advanced Features
-----------------

 * customization
 * manually turn it on and off
 * run specific sections without error reporting
 * ignore files allowing you to avoid highlighting code in your stack trace
 * application files; these are prioritized when an error strikes!
 
![Application Aware Stack Trace](http://i.imgur.com/qdwnb.png)


