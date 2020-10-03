# SIG: Web - website2020 (up to date!) - a super duper amazing project
This is [CompSoc Edinburgh](https://comp-soc.com)'s website, built by SIG:Web.

## Running on your computer
It uses Jekyll. It also works very amazingly nicely with Docker.

If you use Linux or macOS, run `docker-run.sh`. It will automatically build, server, and watch the directory for changes and it will listen on port 4000. 

If you're on Windows (I'm sorry), please contribute some instructions. You'll hopefully be able to read `docker-run.sh` and adapt the commands to play nice with docker-machine, or native Docker if that's your thing.

## Running on your computer without Docker
If you have `bundler` installed, type:

- `bundle`, to install the Gemfile packages
- `bundle exec jekyll serve` to host a local server that will watch the directory for changes

Thanks for visiting!!
