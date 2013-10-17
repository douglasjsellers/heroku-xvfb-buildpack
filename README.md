Heroku buildpack: XVFB
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) of XVFB and xvfb-run(http://www.x.org/archive/current/doc/man/man1/Xvfb.1.xhtml).

Usage
-----

Example usage:

```shell
$ heroku create --stack cedar --buildpack http://github.com/douglasjsellers/heroku-xvfb-buildpack

# or if your app is already created:
$ heroku config:add BUILDPACK_URL=http://github.com/douglasjsellers/heroku-xvfb-buildpack

$ git push heroku master
```

Note
-----

If you're using [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi) to include other buildpacks, you should set environment variable by your own to include following paths.

    PATH="/usr/local/bin:/usr/bin:/bin:/app/vendor/xvfb/bin"
    LD_LIBRARY_PATH="/usr/local/lib:/usr/lib:/lib:/app/vendor/xvfb/lib"
