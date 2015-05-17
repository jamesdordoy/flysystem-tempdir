# Flysystem Adapter for Temporary Directory

[![Build Status](https://img.shields.io/travis/emgag/flysystem-tempdir/master.svg?style=flat-square)](https://travis-ci.org/emgag/flysystem-tempdir)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)


## Installation

```bash
TBD composer require emgag\flysystem-tempdir
```

## Usage


As League\Flysystem\Filesystem wrapper:

```php
use Emgag\Flysystem\Tempdir;
$fs = new Tempdir([$prefix],[$tempdir]);
```


or as Flysystem Adapter:

```php
use Emgag\Flysystem\TempdirAdapter;
use League\Flysystem\Filesystem;

$adapter = new TempdirAdapter([$prefix],[$tempdir]);

$filesystem = new Filesystem($adapter);
```
