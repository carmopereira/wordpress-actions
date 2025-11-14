# workflows disponíveis

- Wordpress Coding Standards
- Re-usable WordPress Actions

# WordPress Coding Standards

✅ PHP (via 10up/wpcs-action)

Não precisa de Composer! 🎉
Verifica WordPress Coding Standards
Anotações automáticas nos PRs
Verifica apenas linhas alteradas (super rápido!)
Standard configurável (WordPress, VIP-Go, 10up-Default)

✅ CSS/SCSS (via Stylelint)

@wordpress/stylelint-config
Regras WordPress oficiais
Ignora minified files

✅ JavaScript (via ESLint)

@wordpress/eslint-plugin
Configurado para jQuery e wp globals
Ignora minified files

# Re-usable WordPress Actions (ainda em fase de teste)

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
