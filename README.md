gulp-jshint-html-reporter
====================

A simple reporter for gulp-jshint that writes it's output to a file.

## Installation

```bash
$: npm install gulp-jshint-html-reporter --save
```

## Usage

```javascript
var gulp = require('gulp');
var jshint = require('gulp-jshint');

gulp.task('lint', function() {
  return gulp.src('./lib/*.js')
    .pipe(jshint())
    .pipe(jshint.reporter('gulp-jshint-html-reporter', {
      filename: __dirname + '/jshint-output.log'
    }));
});

## Options

Plugin options:

Type: `filename`
Default: `"jshint-output.html"`

The filename to write output from jshint. When linting is successfull, the file is not created.

## License

[MIT](http://opensource.org/licenses/MIT) © [Ivan Vesely](ivan.jan.vesely@gmail.com)

## Release History

* 0.1.0 Initial release