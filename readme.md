# Web starter kit

## Get started

To get up and running open up terminal and clone this repository.

    git clone https://github.com/gavlak/web-starter-kit.git
    
After it finished cloning you will need to install all the packages using command:

    npm install
    

## Folder structure

Folder structure is as simple as possible without cluttering the project. Public folder has only one folder, assets. It's because Gulp will take care of everything and in the end there will be only one .css file and one .js file.

```
   ├ /public
   │    ├ /assets
   │    └── index.html  # all compiled jade pages
   │
   ├ /source
   │    ├ /html       # jade templates and pages
   │    ├ /images     # unprocessed images
   │    ├ /js         # javascript files
   │    └ /sass       # SCSS files
   │
   ├── gulpfile.js
   └── package.json
```

## Gulpfile

At the top of the file you can change path configurations.

`dirs` - source and destination directories

`paths` - paths for gulp tasks

`files` - final filenames

### Gulp tasks

`default` - run jade, styles and scripts tasks

`clean` - delete files in public folder

`serve` - start browsersync server from public directory, watch files for changes and auto update website running at `localhost:3000`

Then you should see this webpage in your browser:
![web starter kit screenshot](https://raw.githubusercontent.com/gavlak/web-starter-kit/master/screenshot.png)

`watch` - watch for file changes and runs task

`images` - compress images if possible

##### Internal tasks

`jade` - compile jade files, but ignore `_*.jade` files

`scripts` - compile concatenate all `.js` files into one file

`styles` - compile SCSS to `.css` file

### Jade templates

In `source/html` you will find provided files, with basic templating functionality.

`index.jade` - example page, which uses template

`_config.jade` - variables for changing language, link extensions, etc.

`_mixins.jade` - some basic mixins to make templating easier

`_template.jade` - main template file, loads assets generated by Gulp