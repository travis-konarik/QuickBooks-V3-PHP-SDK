========
Overview
========

Requirements
============

#. PHP 5.6 or greater
#. To use the PHP Guzzle handler, guzzlehttp/guzzle needs to be installed via Composer.
#. To use the cURL handler, you must have a recent version of cURL >= 7.19.7
   compiled with OpenSSL.
   
.. note::

    Intuit has required QuickBooks Online apps to upgrade to TLS 1.1 or above 
    by July 31, 2017 to align with industry best practices for security and data 
    integrity. As of December 31, 2017, the required version will be TLS 1.2 or 
    higher.

.. _installation:


Installation
============

The recommended way to install QuickBooks V3 SDK is with
`Composer <http://getcomposer.org>`_. Composer is a dependency management tool
for PHP that allows you to declare the dependencies your project needs and
installs them into your project.

.. code-block:: bash

    # Install Composer
    curl -sS https://getcomposer.org/installer | php

You can add QuickBooks V3 SDK as a dependency using the composer.phar CLI:

.. code-block:: bash

    composer require quickbooks/v3-php-sdk

Alternatively, you can specify QuickBooks V3 SDK as a dependency in your project's
existing composer.json file:

.. code-block:: js

    {
      "require": {
         "quickbooks/v3-php-sdk": ">=4.0.1"
      }
   }

After installing, you need to require Composer's autoloader:

.. code-block:: php

    require 'vendor/autoload.php';

You can find out more on how to install Composer, configure autoloading, and
other best-practices for defining dependencies at `getcomposer.org <http://getcomposer.org>`_.

.. note::

    If you are not famailar with Composer or Composer is not possible to be used in your enviornment, 
    you can also go to the "releases" tab to download the zip file version of our PHP SDK. 
    See example scripts here https://github.com/intuit/QuickBooks-V3-PHP-SDK/tree/master/src/_Samples for 
    how to make QuickBooks Online API call without Composer. You will need to use the 
    
    .. code-block:: php

        include('../config.php');
        
    to include the necessary autoloader.


License
=======

Licensed using the `Apache License, Version 2.0`
    
  Copyright (c) 2017 Intuit
 
  Licensed under the Apache License, Version 2.0 (the "License");
  you may not use this file except in compliance with the License.
  You may obtain a copy of the License at
 
  http://www.apache.org/licenses/LICENSE-2.0
 
  Unless required by applicable law or agreed to in writing, software
  distributed under the License is distributed on an "AS IS" BASIS,
  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  See the License for the specific language governing permissions and
  limitations under the License.

Contributing
============


Guidelines
----------

1. We are graduatelly changing the code style to utilizes PSR-1, PSR-2, PSR-4, and PSR-7. It will
   take some time, however, all pull requests in the future should follow the same standards.
2. QuickBooks V3 SDK is meant to be lean and fast with very few dependencies. This means
   that not every feature request will be accepted.
3. QuickBooks V3 SDK has a minimum PHP version requirement of PHP 5.6. Pull requests must
   not require a PHP version greater than PHP 5.6 unless the feature is only
   utilized conditionally.



