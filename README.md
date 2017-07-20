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
