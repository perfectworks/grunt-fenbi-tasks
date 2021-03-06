# grunt-fenbi-tasks

Grunt tasks used by [fenbi.com]. To generate jsctags, hash file, etc.

## Getting Started
This is an internal task set used by [fenbi.com], read each source before use it.

Install the module with: `npm install grunt-fenbi-tasks`

```javascript
grunt.initConfig({
    hash: {
        release: {
            src: TEMP_BUILD,
            dest: TARGET_RELEASE,
            urlPrefix: '/s/',
            files: '**/*.*',
            staticMap: TARGET + 'WEB-INF/view/global/StaticMap.vm'
        },

        cdn: {
            src: TEMP_BUILD,
            dest: TARGET + 's/',
            urlPrefix: '//cdn.yuanti.ku/s/',
            files: '**/*.*',
            staticMap: TARGET + 'WEB-INF/view/global/StaticMap.vm'
        }
    },

    jsctags: {
        development: {
            root: SOURCE,
            files: [
                'bootstrap/**/*.js',
                'collection/**/*.js',
                'component/**/*.js',
                'global/**/*.js',
                'model/**/*.js',
                'page/**/*.js',
                'router/**/*.js',
                'task/**/*.js',
                'util/**/*.js'
            ]
        }
    }
});
```

## Documentation
_(Coming soon)_

## Examples
_(Coming soon)_

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [grunt](https://github.com/gruntjs/grunt).

## Release History

`0.1.8` 2013-04-16 Fix data uri in hash task.
`0.1.7` 2013-01-05 Support grunt 0.4.0.
`0.1.6` 2013-01-05 Add `minimize` task with source map support, and add source map support to `hash` task.
`0.1.5` 2012-12-18 Move `handlebars` to `grunt-handlebars-seajs` task.
`0.1.3` 2012-12-07 Rename task `cdn` to `hash`.
`0.1.2` 2012-12-07 Fix combo bug, modify README.md.
`0.1.0` 2012-12-06 First release.

## License
Copyright (c) 2012 PerfectWorks  
Licensed under the MIT license.

[fenbi.com]: http://fenbi.com
[SeaJS]: http://seajs.org
