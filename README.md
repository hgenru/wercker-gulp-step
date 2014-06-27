# gulpjs

A wercker step to execute commands using the gulp-cli.

You should have nodejs installed and you have to add the `gulp` package to your package.json.

# What's new

- Use `gulp-cli` if it is installed in `./node_modules/gulp-cli`

## Example Usage

In your [wercker.yml](http://devcenter.wercker.com/articles/werckeryml/) file under the `build` section: 

``` bash
build:
  steps:
    - hgen/gulp:
        tasks: test
```

## Arguments

### tasks
- type: string
- optional: true
- description: Tasks which should be run. You can use spaces to specify multiple tasks. If no tasks have been specified, then gulp-cli will run the `default` task. 
- example: `tasks: jshint buster`

### gulpfile
- type: string
- optional: true
- description: Specify an alternate gulpfile. By default, gulp looks in the source directory or it's parent directories for the nearest gulpfile.js or gulpfile.coffee file.

### stack
- type: boolean
- optional: true (default: false)
- description: Print a stack trace when exiting with a warning or fatal error.

### verbose
- type: boolean
- optional: true (default: false)
- description: Run gulp in verbose mode
 
### debug
- type: boolean
- optional: true (default: false)
- description: Enable debugging mode for tasks that support it.
