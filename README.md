# Flysystem Adapter for Temporary Directory

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg)](LICENSE)
[![Packagist Version](https://img.shields.io/packagist/v/emgag/flysystem-tempdir.svg)](https://packagist.org/packages/emgag/flysystem-tempdir)

An adapter for the [Flysystem](https://github.com/thephpleague/flysystem) file 
system abstraction library which creates a temporary directory on local filesystem
and which is automatically removed again on object destruct.

## Installation

```bash
composer require emgag/flysystem-tempdir
```

## Usage


As League\Flysystem\Filesystem wrapper:

```php
use Emgag\Flysystem\Tempdir;
$fs = new Tempdir([$prefix],[$tempdir]);
// fully qualified FS path
$fsPath = $fs->getPath();
```


or as Flysystem Adapter:

```php
use Emgag\Flysystem\TempdirAdapter;
use League\Flysystem\Filesystem;

$adapter = new TempdirAdapter([$prefix],[$tempdir]);

$filesystem = new Filesystem($adapter);
```

## License

flysystem-tempdir is licensed under the [MIT License](http://opensource.org/licenses/MIT).

