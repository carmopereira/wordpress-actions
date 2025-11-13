# GamersGrass WordPress Actions

Reusable GitHub Actions workflows para desenvolvimento de plugins WordPress com auto-detecção.

## Quick Start

No teu plugin, cria `.github/workflows/ci.yml`:
```yaml
name: CI/CD

on:
  push:
    branches: [ main ]
    tags: [ '*' ]

jobs:
  workflow:
    uses: gamersgrass/wordpress-actions/.github/workflows/reusable-wordpress-plugin-workflow-autodetect.yml@main
    secrets: inherit
```

## Requisitos

### Headers no Plugin
```php
/**
 * Plugin Name: Nome do Plugin
 * Version: 1.0.0
 * Requires PHP: 8.1
 * Text Domain: nome-do-plugin
 */
```

### Organization Secrets
- `WORDPRESS_SVN_USERNAME`
- `WORDPRESS_SVN_PASSWORD`

## Documentação

Ver documentação completa em: [docs](https://github.com/gamersgrass/wordpress-actions)
