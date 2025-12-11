# Monorepo Builder

Tools to build a Monorepo. Fork of [symplify/monorepo-builder](https://github.com/symplify/monorepo-builder).

## Installation

```bash
composer require monorepo-php/monorepo-builder --dev
```

## Usage

```bash
vendor/bin/monorepo-builder <command>
```

### Available Commands

```bash
# Merge composer.json files
vendor/bin/monorepo-builder merge

# Validate monorepo structure
vendor/bin/monorepo-builder validate

# Release a new version
vendor/bin/monorepo-builder release <version>

# List packages
vendor/bin/monorepo-builder packages
```

## Configuration

Create a `monorepo-builder.php` file in your project root:

```php
<?php

declare(strict_types=1);

use Symplify\MonorepoBuilder\Config\MBConfig;

return static function (MBConfig $mbConfig): void {
    $mbConfig->packageDirectories([
        __DIR__ . '/packages',
    ]);
};
```

## License

MIT

