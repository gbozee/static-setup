# Gulp Set up with live reload

### Gulp & BrowserSync Section
Ensure your have `node >= 4` on your system.

You can download node from [https://nodejs.org/en/download/](https://nodejs.org/en/download/)

You also need to add `node` to your path then open your command line and type `npm`

    git clone <repo>
    npm install -g gulp # if you haven't installed gulp
    npm install -g browser-sync # if you haven't installed browser-sync
    npm install

Edit this line in the `gulpfile.js` to point to the local server url setup

    gulp.task('browserSync', function() {
    browserSync.init(
        [paths.css + '/*.css', paths.js + '*.js', paths.templates + '/*.html'], {
            proxy: '<wordpress localhost url : e.g localhost:8000>',
        });
    });


And finally

    gulp watch

This setup also supports `sass` in case you prefer writing sass to css just create the `sass` directory 
<p>and everything should work as expected</p>

### How to add node to path (Windows)

Go to `control panel -> System -> Advanced System Settings` then environment variables.

From here find the path variable, Go to the end of the line and paste `"C:\Program Files\nodejs\node_modules\npm\bin"` (change the path to the directory to where ever you installed it e.g. if you specifically installed it anywhere change it)