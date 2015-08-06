# content-mapping-sourceadapter-propel #

SourceAdapter for Propel Databases in the [webfactory/content-mapping](https://github.com/webfactory/content-mapping)
mini framework.

## Installation ##

Assuming you already have a working Propel installation, simply

    composer require webfactory/content-mapping-sourceadapter-propel

## Usage ##

```php
use Webfactory\ContentMapping\Synchronizer;
use Webfactory\ContentMapping\SourceAdapter\Propel\GenericPropelSourceAdapter;

$classNameToSynchronize = 'MyClass';
$resultSetMethod = 'doSelectRS';

$sourceAdapter = new GenericPropelSourceAdapter($classNameToSynchronize, $resultSetMethod);

$synchronizer = new Synchronizer($sourceAdapter, $mapper, $destinationAdapter, $logger);
```

If the `GenericPropelSourceAdapter` does not fit your needs, you may find the abstract `PropelSourceAdapter` helpful.

## Credits, Copyright and License ##

This project was started at webfactory GmbH, Bonn.

- <http://www.webfactory.de>
- <http://twitter.com/webfactory>

Copyright 2015 webfactory GmbH, Bonn. Code released under [the MIT license](LICENSE).
