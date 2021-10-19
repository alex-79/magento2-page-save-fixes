# Instalation

Fix for https://github.com/magento/magento2/issues/31007

1. Install package by composer:

`composer require alex-79/magento2-page-save-fixes`

2. Extend composer.json:

```
    "extra": {
        "enable-patching": true,
        "magento-force": "override",
        "composer-exit-on-patch-failure": true,
        "patches": {
            "magento/module-cms": {
                "Fix for https://github.com/magento/magento2/issues/31007": "vendor/alex-79/magento2-cms-save-fixes/vendorPatch/magento/module-cms/Model/PageRepository.patch"
            }
        }
    }
```

3. composer install

`composer install`
