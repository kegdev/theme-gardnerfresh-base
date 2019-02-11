# GardnerFresh_base  - Composer Theme
This theme is a work in progress effort for a Magento 2 theme based on GardnerFresh.com. This theme uses `magento/blank` as a parent.

## Installation
1. Add `"kegdev/gardnerfresh_base": "dev-master"` to the `require`
section of the `composer.json` file in your install.
2. Add the following to the `repositories` section:
```json
"gardnerfresh_base": {
    "type": "git",
    "url": "https://github.com/kegdev/theme-gardnerfresh_base"
}
```
3. Run `composer upgrade`.
4. Go to your install's Admin and navigate to `Content >Themes` and confirm the theme appears.
5. Set your install to use the theme from `Content > Configuration`.

## Optional Configuration

Use grunt? Add this to your `themes.js` normally located at `dev/tools/grunt/configs`.
```json
    gf_base: {
        area: 'frontend',
        name: 'GardnerFresh/base',
        locale: 'en_US',
        files: [
            'css/styles-m',
            'css/styles-l',
            'css/email',
            'css/email-inline',
            'css/source/_extend',
            'css/source/homepage',
            'css/source/default'
        ],
        dsl: 'less'
    }
```
