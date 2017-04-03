## Overview
ChromePhp is a PHP library for the Chrome Logger Google Chrome extension.

This library allows you to log variables to the Chrome console.

## Requirements
- PHP 5 or later

## Installation
1. Install the Chrome extension from: https://chrome.google.com/extensions/detail/noaneddfkdjfnfdakjjmocngnfkfehhd
2. Click the extension icon in the browser to enable it for the current tab's domain
3. Put ChromePhp.php somewhere in your PHP include path
4. Log some data

    ```php
    include 'ChromePhp.php';
    ChromePhp::log('Hello console!');
    ChromePhp::log($_SERVER);
    ChromePhp::warn('something went wrong!');
    ```

More information can be found here:
http://www.chromelogger.com


## Updates by oluwaponle

I added the setEnabled method to enable/disable logging when switching between development and production.

WSE is a shortform of With Set Enabled

    ```php
    include 'ChromePhpWSE.php';
    ChromePhpWSE::setEnabled(true) ;  //false disables logging. Default is false to encourage proper usage and avoid showing logs on production
    ChromePhpWSE::log('Hello console!');
    ChromePhpWSE::log($_SERVER);
    ChromePhpWSE::warn('something went wrong!');
    ```
