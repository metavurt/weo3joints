### What is WEO3Joints?
WEO3Joints is a WordPress theme cloned from [JointsWP][2], which was built with [Foundation 6 (v. 6.2.3)][3].

This theme acts as a representative of some of the design philosophies of [WEO3 Development & Design][1], and is a parent theme for all custom child themes developed for clients of [WEO3 Development & Design][1].

JointsWP started its humble life as a fork of the popular theme Bones, and is now used by thousands of websites globally.

WEO3Joints simply hopes to have a life.

### What comes with WEO3Joints?
WEO3Joints comes pre-baked with all of the great features that are found in the Foundation framework. If it works in Foundation, it will work in WEO3Joints. The theme also includes (but not limited to):

- Foundation Navigation Options
- Motion-UI
- Grid archive templates
- Translation Support
- Gulp Support

### What tools do I need to use WEO3Joints?
While JointsWP enables different forms of management for its theme, WEO3Joints will move forward using Sass, npm and Gulp.

### Getting Started
- Install [node.js](https://nodejs.org).
- Using the command line, navigate to your theme directory
- Run npm install
- Run npm update
- Run npm outdated to verify updates
- Run gulp to confirm everything is working



### File Structure

#### Styles
- styles.css – A file required by WordPress, but not used.

- assets/scss/style.scss – Import all of your Sass files here. This file also imports all Foundation styles from the vendor directory. You can remove whatever components you don’t plan on using.

- assets/scss/_main.scss – This is where you will put most of your custom styles

- assets/scss/_settings.scss – Override Foundation styles and variables

- assets/css/*.css – This is where all of the Sass files will compile. Don’t edit these files directly as they will be overwritten anytime you compile your Sass.

#### Scripts
- assets/js/foundation.js – Foundation JS files. If you’re using Gulp, this compiles all Foundation JavaScript components from vendor/foundation-sites/js. You can select which components you want by making adjustments to the gulpfile.js. This file also comes in a minified form.

- assets/js/scripts.js – This is where all of your custom JavaScript will go. If you’re using Gulp, this compiles all Foundation JavaScript components from assets/js/scripts.. This file also comes in a minified form.

- assets/js/scripts/*.js – If you’re using Gulp, you can place all of your custom JS files here and they will be compiled into the assets/js/scripts.js file.

#### Vendor
- vendor/ – All vendor files are located here. It is not recommended to make changes to these files (except when updating).


### Gulp Tasks
#### Watching Files for Changes
Running gulp watch will watch your assets/js/scripts and assets/sass directories for any changes and automatically run the related tasks.

#### Compiling Sass
Running gulp styles will compile all of your Sass files from your assets/sass directory into the assets/css directory. It will create a minified and non-minified file – by default, the theme will enqueue the non-minified file.

#### Compiling Custom JavaScript
Running gulp site-js will combine all of your custom (non-Foundation) JavaScript files from your assets/js/scripts directory into one file in the assets/js directory.

Running this task will create a minified and non-minified file – by default, the theme will enqueue the non-minified file.

#### Compiling Foundation
Running gulp foundation-js will compile all of your Foundation JavaScript files from your vendor/foundation/js/ directory into the assets/js/min directory. It will create a minified and non-minified file – by default, the theme will enqueue the minified file.

The gulpfile.js allows you to easily select which Foundation files you want to use. By default all Foundation components are loaded.

~~~~
gulp.task('foundation-js', function() {
  return gulp.src([ 
           
          // Foundation core - needed if you want to use any of the components below
          './vendor/foundation-sites/js/foundation.core.js',
          './vendor/foundation-sites/js/foundation.util.*.js',
           
          // Pick the components you need in your project
          './vendor/foundation-sites/js/foundation.abide.js',
          './vendor/foundation-sites/js/foundation.accordion.js',
          './vendor/foundation-sites/js/foundation.accordionMenu.js',
          './vendor/foundation-sites/js/foundation.drilldown.js',
          './vendor/foundation-sites/js/foundation.dropdown.js',
          './vendor/foundation-sites/js/foundation.dropdownMenu.js',
          './vendor/foundation-sites/js/foundation.equalizer.js',
          './vendor/foundation-sites/js/foundation.interchange.js',
          './vendor/foundation-sites/js/foundation.magellan.js',
          './vendor/foundation-sites/js/foundation.offcanvas.js',
          './vendor/foundation-sites/js/foundation.orbit.js',
          './vendor/foundation-sites/js/foundation.responsiveMenu.js',
          './vendor/foundation-sites/js/foundation.responsiveToggle.js',
          './vendor/foundation-sites/js/foundation.reveal.js',
          './vendor/foundation-sites/js/foundation.slider.js',
          './vendor/foundation-sites/js/foundation.sticky.js',
          './vendor/foundation-sites/js/foundation.tabs.js',
          './vendor/foundation-sites/js/foundation.toggler.js',
          './vendor/foundation-sites/js/foundation.tooltip.js',
  ])
  ~~~~


[1]: http://www.weo3.com "Home of WEO3 Development & Design"
[2]: http://www.jointswp.com/ "Home of JointsWP"
[3]: http://foundation.zurb.com/sites "Home of Zurb's Foundation: Sites"
