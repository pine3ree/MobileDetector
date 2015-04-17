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

```
$pimple->get('mobileDetect');

$config->mobileDetect;
$config->isMobile;
$config->isTablet;
$config->isPhone;

$page->mobileDetect;
$page->isMobile;
$page->isTablet;
$page->isPhone;
```

