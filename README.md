# ShadowProject.io

[![Join the chat at https://gitter.im/shadowproject/website](https://badges.gitter.im/shadowproject/website.svg)](https://gitter.im/shadowproject/website?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## Devel & Contributions

There are 2 main branches in this repo:

* master = what's live on [shadowproject.io](https://shadowproject.io)
* development = for devel, live on [lab.shadowproject.io](http://lab.shadowproject.io)


### Sass compiling via Gulp

**Don't edit CSS directly!** This website is using Sass and all CSS changes will be discarded if edited directly. [Learn about Sass](http://sass-lang.com/guide) and [how to compile it to CSS automatically](https://css-tricks.com/gulp-for-beginners/).

If you don't want to mess with Gulp, just edit the Sass files and ask someone else to compile it (e.g. @AllienWorks)

Here's a short version:

- you'll need [NPM](https://nodejs.org/), so install it if you don't
    - don't have Gulp installed? install it via ```sudo npm install gulp -g``` (the "-g" part makes sure its installed globally on your system - you can leave it out)
- install Gulp to the Project: navigate to the Project in Terminal and type ```npm install gulp --save-dev``` (this will download all the modules and dependencies; you need this to run only the first time)
- then install Sass module via ```npm install gulp-sass --save-dev``` (also run just once)
- now all you need to do is start ```gulp``` - it will automatically watch for file changes and compile them immediately (let it run in terminal and try modifying some SCSS and save it)

(There _has_ to be even easier way, but I'm not aware of it ATM. If _you_ know, share pls)

Your terminal output should looks something like this: 

    user@machine:/var/www/html/shadow-website-testing$ gulp
    [10:51:20] Using gulpfile /var/www/html/shadow-website-testing/gulpfile.js
    [10:51:20] Starting 'watch'...
    [10:51:20] Finished 'watch' after 8.18 ms
    [10:51:20] Starting 'default'...
    -- Compiling Sass files automatically
    [10:51:20] Finished 'default' after 36 μs
    [10:51:27] Starting 'sass'...
    [10:51:27] Finished 'sass' after 62 ms

