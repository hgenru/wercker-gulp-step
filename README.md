# gruntjs

A wercker step to execute commands using the grunt-cli.

You should have nodejs installed and you have to add the `grunt` package to your package.json.

# What's new

- Use `grunt-cli` if it is installed in `./node_modules/grunt-cli`

## Example Usage

In your [wercker.yml](http://devcenter.wercker.com/articles/werckeryml/) file under the `build` section: 

``` bash
build:
  steps:
    - grunt:
        tasks: test
```

## Arguments

### tasks
- type: string
- optional: true
- description: Tasks which should be run. You can use spaces to specify multiple tasks. If no tasks have been specified, then grunt-cli will run the `default` task. 
- example: `tasks: jshint buster`

### gruntfile
- type: string
- optional: true
- description: Specify an alternate Gruntfile. By default, grunt looks in the source directory or it's parent directories for the nearest Gruntfile.js or Gruntfile.coffee file.

### stack
- type: boolean
- optional: true (default: false)
- description: Print a stack trace when exiting with a warning or fatal error.

### verbose
- type: boolean
- optional: true (default: false)
- description: Run grunt in verbose mode
 
### debug
- type: boolean
- optional: true (default: false)
- description: Enable debugging mode for tasks that support it.

# Changelog

## 0.1.0

- added: verbose option

## 0.0.9

- Fixed a bug in which `grunt` should have been installed via npm

## 0.0.8

- Use `grunt-cli` if it is installed in `./node_modules/grunt-cli`

## 0.0.7

- always update npm

## 0.0.6

- Remove support for PATH, use cwd instead
 
## 0.0.5

- Initial release
