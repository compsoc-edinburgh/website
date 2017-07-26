# CompSoc website

This is the website for [CompSoc Edinburgh](http://comp-soc.com).

## How to test

### Quick Start - Docker (recommended)

The quickest and easiest way to test, if you have Docker installed, is to run
the following command (make sure your current directory is this repository):

```
docker run --volume=$(pwd):/src:Z --publish 4000:4000 grahamc/jekyll serve --watch -H 0.0.0.0
```

### Native Jekyll

If you do not want to use Docker, you'll need Jekyll and the Gems from the Gemfile.

After installing Ruby and Jekyll, you will also need to `gem install bundler`. Run `bundle install`
to download our gems.

Once you have the prerequisites installed, you need to run `bundle exec jekyll serve` to build the site,
spin up a little webserver and watch the directory for any changes.
