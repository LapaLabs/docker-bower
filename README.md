# docker-bower

The Docker image with installed Bower package manager

## Usage

Clone this repository first to your machine:

``` bash
$ git clone git@github.com:LapaLabs/docker-bower.git
$ cd docker-bower
```

Then build the image from this `Dockerfile`:

``` bash
$ docker build -t my/bower:latest .
```

And run container from this image:

``` bash
$ docker run -it -v /path/to/bower/manifest/:/data/ my/bower:latest
```

where `/path/to/bower/manifest/` is the path to folder with your `bower.json` file.

To run any `Bower` command you should to pass it as argument.
If you want to install `jQuery` library and add it as dependency 
to your `bower.json` file - you could do the next command:

``` bash
$ docker run -it -v /path/to/bower/manifest/:/data/ my/bower:latest install jquery -S
```
