# homebrew-nginx

This repository contains **[nginx][nginx]-related** formulae for [Homebrew][brew],
primarily so that users can use the [HttpHeadersMoreModule][headersmore].

**You will need to [install Homebrew][brew_install] to use this**, see [here][brew_install].

Currently contains replacement (or new) formulae for:

* nginx

[nginx]: http://nginx.org/
[brew]: http://mxcl.github.com/homebrew/
[headersmore]: http://wiki.nginx.org/HttpHeadersMoreModule
[brew_install]: https://github.com/mxcl/homebrew/wiki/installation

## Usage

There are two methods to install packages from this repository.

### Method 1: Tap

Tap the repository into your brew installation

    brew tap mtigas/nginx

You'll notice that `brew install nginx` throws warnings -- this is because
the formula cannot technically replace the original one in Homebrew core.
You can install any of the packages in repo by manually denoting the "tap"
prefix (mtigas/nginx):

	brew install mtigas/nginx/nginx --devel --with-spdy --with-headersmore

### Method 2: Raw URL

First, find the raw URL for the formula you want. For example, the raw URL for
the `nginx` formula is:

    https://github.com/mtigas/homebrew-nginx/raw/master/Formula/nginx.rb

Once you know the raw URL, simply use `brew install [raw URL]`, like so:

    brew install https://github.com/mtigas/homebrew-nginx/raw/master/Formula/nginx.rb

(Due to dependencies, you may need to perform `brew tap mtigas/nginx` as in Method 1.)
