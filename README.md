[The Silver Searcher][] is a speedy code searching tool. This repository contains the paraphernalia required for packaging The Silver Surfer on [Cygwin][].

Usage
-----

    cygport ag.cygport download prep compile test install package upload

Test failures
-------------

Currently (as of v0.32.0) the following tests fail:

* `column.t`: This also fails on my CentOS box, so it doesn't appear to be Cygwin-specific.
* `ignore_extensions.t`: This also fails on my CentOS box, so it doesn't appear to be Cygwin-specific.
* `one_device.t`: This _is_ Cygwin-specific, but I suspect it's a false failure and Cygwin just doesn't report `/dev/shm` as being a separate device in the way it normally is on Linux.

[The Silver Searcher]: http://geoff.greer.fm/ag/
[Cygwin]: https://cygwin.com/
