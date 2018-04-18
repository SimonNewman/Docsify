# Magento

## Prerequisites

[Node.js](development/node.md) should be installed and Magento should be set to developer mode.

## Grunt

Magento has built-in Grunt tasks configured but a small amount of initial setup is required.

After installing Magento and creating your theme, navigate to the Magento directory;

1. Install Grunt CLI tool globally `npm install -g grunt-cli`
2. Rename `Gruntfile.js.sample` to `Gruntfile.js`
3. Rename `package.json.sample` to `package.json`
4. Run `npm install`
5. Add your theme to Grunt configuration. To do this, in the `dev/tools/grunt/configs/themes.js` file, add your theme to module.exports like following:

```javascript
<theme>: {
        area: 'frontend',
        name: '<Vendor>/<theme>',
        locale: 'en_GB',
        files: [
            'css/styles-m',
            'css/styles-l'
        ],
        dsl: 'less'
    }
```

All commands should be run from the root directory of the Magento installation.

In the following examples, change <theme> to the name of your theme.

> `grunt clean:<theme>`

Removes the theme related static files in the pub/static and var directories.

> `grunt exec:<theme>`

Republishes symlinks to the source files to the `pub/static/frontend/<Vendor>/<theme>/<locale>` directory.

> `grunt less:<theme>`

Compiles .css files using the symlinks published in the `pub/static/frontend/<Vendor>/<theme>/<locale>` directory

> `grunt watch`

Tracks the changes in the source files, recompiles .css files, and reloads the page in the browser pages (you need to have LiveReload installed for you browser)
