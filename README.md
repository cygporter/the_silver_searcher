[The Silver Searcher][] is a speedy code searching tool. This repository contains the paraphernalia required for packaging The Silver Surfer on [Cygwin][].

Usage
-----

    cygport ag.cygport download prep compile test install package upload

Test failures
-------------

Currently (as of v0.31.0-1) the following tests fail:

* `column.t` and `ignore_extensions.t`: This also fails on my CentOS box, so it doesn't appear to be Cygwin-specific.  These tests are bugged, as they rely on non-portable `echo` behaviour.  [Reported upstream](https://github.com/ggreer/the_silver_searcher/issues/866).
* `one_device.t`: This _is_ Cygwin-specific, but it's a false failure as Cygwin just doesn't report `/dev/shm` as being a separate device in the way it normally is on Linux.  [Reported upstream](https://github.com/ggreer/the_silver_searcher/issues/864).

[The Silver Searcher]: http://geoff.greer.fm/ag/
[Cygwin]: https://cygwin.com/
