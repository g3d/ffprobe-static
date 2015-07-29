# ffprobe-static

ffprobe static binaries for Mac OSX and Linux and Windows

[![build status](https://secure.travis-ci.org/eugeneware/ffprobe-static.png)](http://travis-ci.org/eugeneware/ffprobe-static)

## Installation

This module is installed via npm:

``` bash
$ npm install ffprobe-static
```

## Example Usage

Returns the path of a statically linked ffprobe binary on the local filesystem.

``` js
var ffprobe = require('ffprobe-static');
console.log(ffprobe.path);
// ~/ffprobe-static/bin/darwin/x64/ffprobe
```

Currently supports Mac OS X (64-bit), Linux (32 and 64-bit) and Windows
(32 and 64-bit).

Currently version `2.5.3` is installed for Mac and Linux, and `2.5.2` for
Windows.

I pulled the versions from the ffprobe static build pages linked from the
official ffprobe site. Namely:

* [64 bit Mac OSX](https://evermeet.cx/ffprobe/)
* [64 bit Linux](http://johnvansickle.com/ffprobe/)
* [32 bit Linux](http://johnvansickle.com/ffprobe/)
* [64 bit Windows](http://ffprobe.zeranoe.com/builds/win64/static/)
* [32 bit Windows](http://ffprobe.zeranoe.com/builds/win32/static/)

NB: Open to pull requests to update this module with the latest versions.

Ideally I'd like to dynamically pull the latest version down, but this requires
access to 7-zip which and being able to untar `xz` files.

And I couldn't find a good js-only decoders for these files either.

So, for now it's just embedded binaries.
