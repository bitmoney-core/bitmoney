Bitmoney Core
=====================================

What is Bitmoney?
----------------

Bitmoney is a digital currency based off of Litecoin that enables instant payments to
anyone, anywhere in the world. Bitmoney uses peer-to-peer technology to operate
with no central authority: managing transactions and issuing money are carried
out collectively by the network. Bitmoney Core is the name of open source
software which enables the use of this currency.

License
-------

Bitmoney Core is released under the terms of the MIT license. See [LICENSE](LICENSE) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

Any volunteers are free to contribute their own work on separate branches. Bitmoney is, and always will be, a completely open-source project built by the community.

There are 2 types of branches in this repository:

- **master:** Stable, contains the latest version for the "average user"
- **development:** Unstable, contains new code which may bring bugs and glitches. Not recommended for most users.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

Bitmoney Supply
-------

There will be approximately 200,000,000 coins at launch (Summer 2018). Each subsequent block will grant a number of coins determined by how many blocks have previously been mined. This is to encourage miners to continue to secure the network and make up for lost wallets on hard drives/phones/lost encryption passwords/etc.


Building Bitmoney
-------
Documents will be added later to guide you through building Bitmoney's executables.


Development tips and tricks
---------------------------

**Compiling for debugging**

Run configure with the --enable-debug option, then make.

**debug.log**

If the code is behaving strangely, take a look in the debug.log file in the data directory;
error and debugging messages are written there.

The -debug=... command-line option controls debugging; running with just -debug will turn
on all categories (and give you a very large debug.log file).

The Qt code routes qDebug() output to debug.log under category "qt": run with -debug=qt
to see it.

**testnet and regtest modes**

If your tests require multi-machine/internet usage, run with the -testnet option to use fake bitmoney on the test network.

If you are testing something that can run on one machine, run with the -regtest option.
