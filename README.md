# MobileDetector

Mobile device detection using https://github.com/serbanghita/Mobile-Detect

## Install

- Download/install composer and add "mobiledetect/mobiledetectlib": "2.8.*" package

- include vendor/autoload.php at the end of your site/config.php

- optional but recommended: protect your vendor directory from web access, add
    ```
    RewriteCond %{REQUEST_URI} ^/vendor/.*$ [OR]
    ```
    before the other conditions in your pw .htaccess file

- Install this module using PW admin interface

- You can now access the following variables:

    ```php
    $pimple->get('mobileDetect'); // Detection\MobileDetect instance

    // $config is available for application using processwire api even if not
    // rendering a $page
    $config->mobileDetect; // same Detection\MobileDetect instance

    $config->isMobile; // bool
    $config->isTablet; // bool
    $config->isPhone;  // bool

    $page->mobileDetect; // same Detection\MobileDetect instance

    $page->isMobile; // bool
    $page->isTablet; // bool
    $page->isPhone;  // bool
    ```

