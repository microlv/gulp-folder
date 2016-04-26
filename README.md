# gulp-folder
easy to build your framework

* npm install

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
