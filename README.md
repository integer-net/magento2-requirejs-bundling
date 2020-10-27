# magento2-requirejs-bundling
Tools, patches and snippets for Magento 2 RequireJS Bundling

This repository will accompanies our "Ultimate guide to Magento 2 JavaScript bundling" blog post on https://www.integer-net.com/ultimate-guide-magento-2-javascript-bundling/.

## RequireJS bundling config
There's an example `requirejs-bundle-config.js` file here [/requirejs-bundle-configuration](/requirejs-bundle-configuration)

If you look at the diff of the last commit, you can see the changes we made to the default bundle confuration generated by the [M2 DevTools extension](https://github.com/magento/m2-devtools/)

## Patches

! Starting version 2.3.6 patches are no longer needed.

To use RequireJS bundling in Magento 2 (up to version 2.3.5) you need a few patches:

- https://github.com/magento/magento2/pull/25587
- https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574

You can download them from this repository and place them in the root of your Magento project.
Next install `cweagans/composerpatches`.
```bash
composer require cweagans/composer-patches
```

Then add this to your `composer.json` file under `extra`.

For Magento 2.3.1:
```json
"extra": {
        "magento-force": "override",
        "composer-exit-on-patch-failure": true,
        "patches": {
            "magento/magento2-base": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M231/github-pr-4721-base.diff",
                "Refactor JavaScript mixins module https://github.com/magento/magento2/pull/25587": "patches/composer/M231/github-pr-25587-base.diff"
            },
            "magento/module-braintree": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M231/github-pr-4721-braintree.diff"
            },
            "magento/module-catalog": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M231/github-pr-4721-catalog.diff"
            },
            "magento/module-customer": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M231/github-pr-4721-customer.diff"
            },
            "magento/module-msrp": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M231/github-pr-4721-msrp.diff"
            },
            "magento/module-paypal": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M231/github-pr-4721-paypal.diff"
            },
            "magento/module-theme": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M231/github-pr-4721-theme.diff"
            }
        }
    }
```
For Magento 2.3.2:
```json
"extra": {
        "magento-force": "override",
        "composer-exit-on-patch-failure": true,
        "patches": {
            "magento/magento2-base": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M232/github-pr-4721-base.diff",
                "Refactor JavaScript mixins module https://github.com/magento/magento2/pull/25587": "patches/composer/M232/github-pr-25587-base.diff"
            },
            "magento/module-braintree": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M232/github-pr-4721-braintree.diff"
            },
            "magento/module-catalog": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M232/github-pr-4721-catalog.diff"
            },
            "magento/module-customer": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M232/github-pr-4721-customer.diff"
            },
            "magento/module-msrp": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M232/github-pr-4721-msrp.diff"
            },
            "magento/module-paypal": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M232/github-pr-4721-paypal.diff"
            },
            "magento/module-theme": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M232/github-pr-4721-theme.diff"
            }
        }
    }
```

For Magento 2.3.3:
```json
"extra": {
        "magento-force": "override",
        "composer-exit-on-patch-failure": true,
        "patches": {
            "magento/magento2-base": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M233/github-pr-4721-base.diff",
                "Refactor JavaScript mixins module https://github.com/magento/magento2/pull/25587": "patches/composer/M233/github-pr-25587-base.diff"
            },
            "magento/module-braintree": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M233/github-pr-4721-braintree.diff"
            },
            "magento/module-catalog": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M233/github-pr-4721-catalog.diff"
            },
            "magento/module-customer": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M233/github-pr-4721-customer.diff"
            },
            "magento/module-msrp": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M233/github-pr-4721-msrp.diff"
            },
            "magento/module-paypal": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M233/github-pr-4721-paypal.diff"
            },
            "magento/module-theme": {
                "[Performance] Fix missing shims and phtml files with mage-init directives (https://github.com/magento/magento2/commit/db43c11c6830465b764ede32abb7262258e5f574)": "patches/composer/M233/github-pr-4721-theme.diff"
            }
        }
    }
```

For Magento 2.3.4 abd 2.3.5:
```json
"extra": {
        "magento-force": "override",
        "composer-exit-on-patch-failure": true,
        "patches": {
            "magento/magento2-base": {
                "Refactor JavaScript mixins module https://github.com/magento/magento2/pull/25587": "patches/composer/M234/github-pr-25587-base.diff"
            }
        }
    }
```

For Magento 2.3.4 abd 2.3.6:
NO PATCHES NEEDED
