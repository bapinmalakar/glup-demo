# glup-demo

Simple example for Gulp.js

1. Install Node.js, if not present
2. npm i --g gulp
3. git clone https://github.com/bapinmalakar/glup-demo.git
4. Move to the project folder
5. npm i
6. gulp task_name

Some Basic description:

gulpfile.js => configure are written here and should root of the project

Packages
npm gulp
nam gulp-newer
nam gulp-noop => for do nothing

//for images
npm gulp-imagegin => for compress images

//for html
npm gulp-htmlclean => for html in prod

//for js
npm gulp-deporder => check all dependency
npm gulp-concat => all script file in single file(main.js) 
npm gulp-strip-debug => remove all console & debug
npm gulp-terser => minimise code with es6 comparable
npm gulp-sourcemaps => append source map when in dev mode

//for scss
npm gulp-sass => to process sass
npm postcss-assets => to resolve all file dependency ex: background: resolve('image.png');
npm autoprefixer => automatically add  vendor prefix to css properties
npm css-mqpacker 
npm cssnano => minified css

glup.src(input_folder) => read files from and given to glue for process
gulp.dest(output_folder) => put all process file here

.pipe() for function chaining in gulp

each function are task
function image()
function html()
gulp.series(image, html)=> process each task one after another

es: exports.build_prject = glup.series(image, html)

glup build_project for run gulp

running all task parallel
exports.build_project = gulp.parallel(exports.html, exports.css, exports.js);

gulp.watch(folder_name, function_name)
 to watch that any file changes are happened or not, if happen then build again 


