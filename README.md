DOWNLOAD
========

* Cranepay [CRP] Source code on github https://github.com/cranepay/cranepay-core
* Cranepay [CRP] Download Releases https://github.com/cranepay/cranepay-core/releases/
* Algo YeSPoWer 


Useful links
============

* Mining Pool:    http://pool.cranepay.io fee 0%.
* BlockExplorer:  http://explorer.cranepay.io/

* RoadMap:        http://cranepay.io/roadmap/
* Website:        http://cranepay.io/

* Twitter:        https://twitter.com/cranepay_io
* Telegram   :    http://t.me/cranepay
* Telegram/RU:    http://t.me/cranepayru
* Telegram/ES:    http://t.me/cranepayes
* Telegram/DE:    http://t.me/cranepayde


Cranepay Core integration/staging tree
=====================================

* Copyright (c) 2017-2019 Cranepay Core Developers
* Copyright (c) 2009-2018 Bitcoin Core Developers
* Copyright (c) 2013-2017 Dash Developers (DarkGravityWave3)
* Copyright (c) 2014-2018 Alexander Peslyak (YesPoWer Original)

Development tips and tricks
----------------------------

**compiling for debugging**

Run configure with the --enable-debug option, then make. Or run configure with
CXXFLAGS="-g -ggdb -O0" or whatever debug flags you need.

**debug.log**

If the code is behaving strangely, take a look in the debug.log file in the data directory;
error and debugging message are written there.

The -debug=... command-line option controls debugging; running with just -debug will turn
on all categories (and give you a very large debug.log file).

The Qt code routes qDebug() output to debug.log under category "qt": run with -debug=qt
to see it.

**testnet and regtest modes**

Run with the -testnet option to run with "play cranepays" on the test network, if you
are testing multi-machine code that needs to operate across the internet.

If you are testing something that can run on one machine, run with the -regtest option.
In regression test mode blocks can be created on-demand; see qa/rpc-tests/ for tests
that run in -regest mode.

**DEBUG_LOCKORDER**

CranePay Core is a multithreaded application, and deadlocks or other multithreading bugs
can be very difficult to track down. Compiling with -DDEBUG_LOCKORDER (configure
CXXFLAGS="-DDEBUG_LOCKORDER -g") inserts run-time checks to keep track of what locks
are held, and adds warning to the debug.log file if inconsistencies are detected.


License
-------

Cranepay Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/cranepay/cranepay-core/tags) are created
regularly to indicate new official, stable release versions of CranePay Core.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

Translations
------------

Changes to translations as well as new translations can be submitted to
[CranePay Core's crane-locale repository](https://github.com/cranepay/core-locale).

**Important**: We do not accept translation changes as GitHub pull requests in main repository.

