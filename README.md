# grunt-sass2scss

> Convert Sass files to SCSS files with sass2scss

[![Analytics](https://ga-beacon.appspot.com/UA-2643697-15/grunt-sass2scss/index)](https://github.com/igrigorik/ga-beacon)
[![Dependency Status](https://img.shields.io/david-dm/paazmaya/grunt-sass2scss.svg?style=flat-square)](https://david-dm.org/paazmaya/grunt-sass2scss)
[![devDependency Status](https://img.shields.io/david-dm/paazmaya/grunt-sass2scss/dev-status.svg?style=flat-square)](https://david-dm.org/paazmaya/grunt-sass2scss#info=devDependencies)
[![Built with Grunt](http://img.shields.io/badge/Grunt-0.4-blue.svg?style=flat-square)](http://gruntjs.com/)

## Getting Started

This plugin requires Grunt `~0.4` and `sass2scss` binary to be available either via PATH or defined via configuration.

The `sass2scss` tool can only [be compiled from sources](https://github.com/mgreter/sass2scss).

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-sass2scss --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-sass2scss');
```

## The "sass2scss" task

### Overview
In your project's Gruntfile, add a section named `sass2scss` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  sass2css: {
    options: {
      // Task-specific options go here.
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    },
  },
});
```

### Options

#### options.binPath

Type: `String`

Default value: `'sass2scss'`

Path to the `sass2scss` binary, which by default is assumed to be found from
the system PATH.

#### options.args

Type: `Array`

Default value: `[]`

Command line options for the `sass2scss` command line utility.

```
-p, --pretty       pretty print output
-c, --convert      convert src comments
-s, --strip        strip all comments
-k, --keep         keep all comments
-h, --help         help text
-v, --version      version information
```

For example to set pretty printing and to keep comments, use `['-p', '-k']`, or
`['pretty', 'keep']`. The leading dashes are optional and added automatically when missing.

### Usage Examples

#### Default Options

```js
grunt.initConfig({
  sass2css: {
     defaultOptions: {
        files: {
          'tmp/default-1.scss': ['test/fixtures/styles-1.sass']
        }
      }
  }
});
```


## Contributing

In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/), via `grunt test` command.

## Release History

* v0.1.0 (2015-01-15) Doing what is promised, when `sass2scss` is available

