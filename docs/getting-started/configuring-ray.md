---
title: Configuring Ray
weight: 4
---

You can optionally configure Ray by creating a file named `ray.php` in your project directory.  We recommend putting `ray.php` in your `.gitignore` so your fellow developers can use their own configuration.

Ray will also look for `ray.php` in all parent directories of your project. To configure multiple Ray for multiple projects in one go, you could create a `ray.php` file in the directory where all your projects reside in.

In framework agnostic projects you can use this template.

```php
// save this in a file called "ray.php"

return [
    /*
     *  The host used to communicate with the Ray app.
     */
    'host' => 'localhost',

    /*
     *  The port number used to communicate with the Ray app. 
     */
    'port' => 23517,
    
    /*
     *  Absolute base path for your sites or projects in Homestead, Vagrant, Docker, or another remote development server.
     */
    'remote_path' => null,
    
    /*
     *  Absolute base path for your sites or projects on your local computer where your IDE or code editor is running on. 
     */
    'local_path' => null,
];
```


For Laravel projects use this template:

```php
// save this in a file called "ray.php"

return [
    /*
     * This settings controls whether data should be sent to Ray.
     * 
     * By default, `ray()` will only transmit data in non-production environments.
     */
    'enable' => true,

    /*
     * When enabled, all things logged to the application log
     * will be sent to Ray as well.
     */
    'send_log_calls_to_ray' => true,

    /*
     * When enabled, all things passed to `dump` or `dd`
     * will be sent to Ray as well.
     */
    'send_dumps_to_ray' => true,
    
    /*
     *  The host used to communicate with the Ray app.
     */
    'host' => 'localhost',
    
    /*
     *  The port number used to communicate with the Ray app. 
     */
    'port' => 23517,
    
    /*
     *  Absolute base path for your sites or projects in Homestead, Vagrant, Docker, or another remote development server.
     */
    'remote_path' => null,
    
    /*
     *  Absolute base path for your sites or projects on your local computer where your IDE or code editor is running on. 
     */
    'local_path' => null,
];
```
