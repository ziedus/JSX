NAME [![Build Status](https://secure.travis-ci.org/jsx/JSX.png)](http://travis-ci.org/jsx/JSX)
=======================

JSX - Object-oriented, statically-typed programming language

INSTALLATION
=======================

The JSX compiler requires `node.js` v0.6.19 or later, and the SDK
also requires Perl 5.10.0 or later.

To setup JSX SDK , type the following command:

    git clone git://github.com/jsx/JSX.git
    cd JSX
    make setup

To install jsx command, just make a link of `bin/jsx` to `~/bin`.

    ln -s "$PWD/bin/jsx" ~/bin

If you use Windows, `npm install -g .` might be better, though.

COMPILATION
=======================

There's `bin/jsx` command to compile JSX source code into JavaScript.

Type the following commands and see what happens:

    # run Hello World in JSX
    bin/jsx --run example/hello.jsx

    # display compiled code to stdout
    bin/jsx example/hello.jsx

    # compile it with fully optimizations
    bin/jsx --release example/hello.jsx

    # compile a program for node, execute it later
    bin/jsx --executable node --output hello.jsx.js example/hello.jsx
    ./hello.jsx.js # displays "Hello, world!"

    # run a test, calling _Test#test*()
    bin/jsx --test example/import.jsx # import.jsx has _Test

`jsx --help` shows how to to use the jsx command.

TESTING
=======================

There are unit tests in `t/` directory. For server side tests, just type the following command:

    make test
    # or
    make test JOBS=2

WEB INTERFACE
=======================

There's a web interface, which compiles JSX source on browsers.
Type the following commands to use the web interface.

    make web
    make server # to run an HTTP daemon
    open http://localhost:5000/

EXAMPLES
=======================

There are examples in `example/` and `web/example/`.

RESOURCES
=======================

* [JSX Wiki](https://github.com/jsx/JSX/wiki)

