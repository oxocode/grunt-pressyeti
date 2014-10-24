# grunt-pressyeti

> Create a WordPress theme with [grunt-init][].

[grunt-init]: http://gruntjs.com/project-scaffolding

## Installation
If you haven't already done so, install [grunt-init][].

Once grunt-init is installed, place this template in your `~/.grunt-init/` directory. It's recommended that you use git to clone this template into that directory, as follows:

### Linux/Mac Users

```
git clone git@github.com:oxocode/grunt-pressyeti.git ~/.grunt-init/pressyeti
```

### Windows Users

```
git clone git@github.com:oxocode/grunt-pressyeti.git ~%/.grunt-init/pressyeti
```

## Usage

At the command-line, cd into an empty directory, run this command and follow the prompts.

```
grunt-init pressyeti
```

_Note that this template will generate files in the current directory, so be sure to change to a new directory first if you don't want to overwrite existing files._

Install the NPM modules required to actually process your newly-created project by running:

```
npm install
```

## Scaffold

After running the init command above, you will be presented with a standard directory structure similar to:

    /theme
    .. /assets
    .. .. /css
    .. .. .. /src
    .. .. .. /sass
    .. .. .. /less
    .. .. /js
    .. .. .. /src
    .. /bower_components
    .. .. /fastclick
    .. .. /foundation
    .. .. .. /css
    .. .. .. /js
    .. .. .. /scss
    .. .. .. .. /foundation
    .. .. .. .. .. /components
    .. .. /jquery
    .. .. /jquery-placeholder
    .. .. /jquery.cookie
    .. .. /modernizr
    .. /images
    .. .. /src
    .. /includes
    .. /languages
    .. .. theme.pot
    .. .gitignore
    .. Gruntfile.js
    .. footer.php
    .. functions.php
    .. header.php
    .. humans.txt
    .. index.php
    .. screenshot.png
    .. style.css

### CSS vs Sass vs LESS

Depending on how you answer the prompt regarding the use of a preprocessor, you will either have a `/src` directory (CSS), a `/sass` directory (Sass), or a `/less` directory (LESS) under your normal `/css` directory.  The goal here is that you only ever edit files in the related source directory and Grunt will automatically build and minify your final stylesheets directly in `/css`.

If you're using Sass or Less, the raw files will be processed into `/css/filename.css` and minified into `/css/filename.min.css`.

If you're using vanilla CSS, the source files will be minified into `/css/filename.min.css`.

*Note:* The `style.css` file in the root of the directory shouldn't contain any style definitions. It's used for populating information on WordPress' themes page only. Your theme's style information should go in the appropriate source directory for your preprocessor under `/assets/css`.

### JavaScript

You should only ever be modifying script files in the `/js/src` directory.  Grunt will automatically concatenate and minify your scripts into `/js/filename.js` and `/js/filename.min.js`.  These generated files should never be modified directly.

### Images

The `/img/src` directory exists only to allow you to keep track of source files (like PSDs or separate images that have been merged into sprites).  This helps keep source files under version control, and allows you to bundle them with the distribution of your new GPL plugin.

### Foundation

You can update to the latest version of Foundation by running:

```
bower update
```

## Release History

 * 2014-10-24   v0.1.0   Initial public release