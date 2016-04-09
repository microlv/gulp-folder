# gulp-folder
easy to build your framework

Adjusted so files are not discarded in through2 callback.

Might have a nasty side effect of creating not intended folders if uses src with globs, so it might be something to look into later.

```js

gulp.task('fw', function () {
    return gulp.src('demo.js').pipe(folder({
        root: './build',
        folders: {
            config: './config',
            css: './css',
            images: './images',
            js: './js',
            services: './services',
            widget: {
                grid: './widget/grid',
                validator: './widget/validator'
            }
        }
    }))
        .pipe(gulp.dest('build/framework'));
});

```
