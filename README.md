# GardnerFresh_base  - Composer Theme
This theme is a work in progress effort for a Magento 2 theme based on GardnerFresh.com. This theme uses `magento/blank` as a parent.

![alt text](https://github.com/kegdev/theme-gardnerfresh-base/blob/master/media/preview.jpg "GardnerFresh_base")

## Installation
1. Add `"kegdev/gardnerfresh_base": "dev-master"` to the `require`
section of the `composer.json` file in your install.
2. Add the following to the `repositories` section:
```json
"gardnerfresh_base": {
    "type": "git",
    "url": "https://github.com/kegdev/theme-gardnerfresh-base"
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
## Setup

As of this release, you will need to manually add two static blocks needed for the homepage. [XML reference](https://github.com/kegdev/theme-gardnerfresh-base/blob/master/Magento_Theme/page_layout/homepage.xml)
1. `homepage-featured` - This occupies the hero section - currently a static span within a div. See the [source](https://github.com/kegdev/theme-gardnerfresh-base/blob/04025914155e2046b9fd723f516c9105673c5c0d/web/css/source/homepage.less#L82) for information on structure and font usage.
2. `homepage-products` - This renders products on the homepage. This utilizes the Catalog product List widget targeted to a specific category and the output is customizeable. See a [tutorial](https://www.simicart.com/blog/magento-featured-products/) on the process for more info.

## To Do
1. Mobile view has not been addressed in `_extend` imports. At all.
2. Add setup scripts for static blocks.

Enjoy this work in progress. :)
