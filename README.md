# End-user documentation sources and generator

This repository contains the markdown sources for the documentation for Atomist.

## Releasing

When a push is made to this repository, the entire documentation is
built again via a [Travis][travis] job.  The documentation is
generated from markdown using [mkdocs][].

[travis]: https://travis-ci.com/atomisthq/end-user-documentation
[mkdocs]: http://www.mkdocs.org/

If the build is triggered by a tag of the form `M.N.P`, the site will
be pushed to the [Atomist GitHub Pages][pages] repository and served
by GitHub at http://atomisthq.github.io and https://docs.atomist.com .

[pages]: https://github.com/atomisthq/atomisthq.github.io

## Build and serve the documentation locally

Generally speaking, you probably do not need to do anything
with this repository aside from pushing markdown content.

However, if you want to make a change to the HTML template
or serve the doc locally before a push, you should follow the
next steps to gear up properly your environment.

First [install Python](https://github.com/Homebrew/brew/blob/master/share/doc/homebrew/Homebrew-and-Python.md)

```
$ brew install python3
```
or

```
$ sudo apt-get install python3
$ curl -O https://bootstrap.pypa.io/get-pip.py
$ sudo python3.5 get-pip.py
```

Then create a virtual environment to host the dependencies:

```
$ pip3 install virtualenv
$ mkdir ~/.venvs
$ echo "export PIP_REQUIRE_VIRTUALENV=true" >> ~/.bashrc
$ source ~/.bashrc
$ virtualenv -p `which python3` ~/.venvs/userdocs
```

Every time you want to work on this repository,
you shall activate that virtualenv in your terminal:

```
$ source ~/.venvs/userdocs/bin/activate
```

Now that the virtual environment is created, we can
install the dependencies into it:

```
$ pip3 install -r requirements.txt
```

You can now serve the documentation locally by running:

```
$ mkdocs serve
```

If all goes well, you can browse the documentation at
http://127.0.0.1:8000 .

## Conditions of use

This documentation build process is provided to the public purely for
the purpose of testing documentation changes before submitting pull
requests to the appropriate Atomist repository.

The documents produced by this build process may be published only on
http://docs.atomist.com. They may not be published in any other form
or on any other website without explicit permission.
