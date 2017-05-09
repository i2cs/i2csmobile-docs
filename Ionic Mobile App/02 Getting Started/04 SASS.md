## SASS

Here we talk about how to compile SASS in i2CSMobile app
----

### SASS Files
Inside `www` folder of the project, we have a `css` folder which contains all the styling related content (i.e., css, sass, icons and fonts). We already included few css files for cusomizations.

> `www/css/style-main.scss` is the main entry point to the sass files. it contains all the color variables and controller style variables like border radius, default width etc. `$positive` is the main color of the theme. most of the css colors automatically build depending on the color of the `$positive` variable.

> `www/css/custom.css` is the place where you can write your own `css` overrides.

> `www/css/style-main.css` and `www/css/style-main.min.css` are auto generated files. Please don't make any manual changes to these files as with next `sass` build all your manual changes might overwrite.

> `www/css/scss/custom.scss` is the place for your own `sass` styles.

### Gulp Task to Compile SASS
Once you are done with `sass` changes, you have to run the following command to compile the sass into css. The gulp task will get all `scss` files and compile them and output to `www/css/style-main.css` and minified output to `www/css/style-main.min.css`

```
Prerequisite : Install gulp on your machine. Please install gulp globally by running

npm install gulp -g

```

1.	Open CMD

2.	Go to project path. (where `gulpfile.js` located)

3.	Run following command
	`gulp sass`
