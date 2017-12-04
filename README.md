# JS Beautifier

[JS Beautifier](https://github.com/beautify-web/js-beautify) in a Docker container for cleaning up your HTML, CSS, and JavaScript. This image exposes the CLI version of [jsbeautifier.org](http://jsbeautifier.org/).

## Usage

If you have a JavaScript file `ugly.min.js` that needs beautification:

```Shell
$ docker run -i asnelling/jsbeautifier < ugly.min.js > pretty.js
```

### Input

With the `-i` flag after `docker run`, your ugly code is read from standard input, which is the file `ugly.min.js` in the above example.

**Or,** pass a file name that exists within the running container, like so:

```Shell
$ docker run -v /path/to/ugly.min.js:/input.js asnelling/jsbeautifier input.js > pretty.js
```

### Output

Your prettified JavaScript is printed to standard output, so pipe away!

### Options

Refer to upstream author's [GitHub page](https://github.com/beautify-web/js-beautify).

### Tags

- [`1.7python-jessie`, `latest`, (python/jessie/Dockerfile)](https://github.com/asnelling/jsbeautifier-docker/blob/master/python/jessie/Dockerfile)
- [`1.7python-slim` (python/jessie/Dockerfile)](https://github.com/asnelling/jsbeautifier-docker/blob/master/python/slim/Dockerfile)
- [`1.7python-stretch` (python/jessie/Dockerfile)](https://github.com/asnelling/jsbeautifier-docker/blob/master/python/stretch/Dockerfile)
- [`1.7python-alpine` (python/jessie/Dockerfile)](https://github.com/asnelling/jsbeautifier-docker/blob/master/python/alpine/Dockerfile)
- [`1.7js-jessie`, (js/jessie/Dockerfile)](https://github.com/asnelling/jsbeautifier-docker/blob/master/js/jessie/Dockerfile)
- [`1.7js-slim`, (js/jessie/Dockerfile)](https://github.com/asnelling/jsbeautifier-docker/blob/master/js/slim/Dockerfile)
- [`1.7js-stretch`, (js/jessie/Dockerfile)](https://github.com/asnelling/jsbeautifier-docker/blob/master/js/stretch/Dockerfile)
- [`1.7js-alpine`, (js/jessie/Dockerfile)](https://github.com/asnelling/jsbeautifier-docker/blob/master/js/alpine/Dockerfile)

If you'd like to use the
