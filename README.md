# CompSoc website

This is the website for [CompSoc Edinburgh](http://comp-soc.com).

## How to test

The quickest and easiest way to test, if you have Docker installed, is to run
the following command (make sure your current directory is this repository):

```
docker run --volume=$(pwd):/src:Z --publish 4000:4000 grahamc/jekyll serve --watch -H 0.0.0.0
```

If you do not want to use Docker, a basic installation of Jekyll will work.
Once you have Jekyll installed, you just need to run `jekyll serve` to try
out this website on your own machine.

## Gulp/BrowserSync Pipeline

Alternatively if you have npm and Jekyll installed on your machine, you can use the Gulp pipeline which auto-prefixes CSS
and includes BrowserSync to automatically reload/inject changed CSS into your browser. It also allows testing across muliple
devices with any actions performed on any of the browsers displaying the site being mirrored across (eg scrolling, buttons, 
form fills)

    1. run `npm install -g gulp` (may need sudo)
    2. run `npm install` while in the project root to grab dependencies
    3. run `gulp` while in project root to build Jekyll site, start BrowserSync and watch for changes in source