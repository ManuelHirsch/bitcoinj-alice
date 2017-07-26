# Multibit is Deprecated - Do Not Use

Wednesday, July 26, 2017

Dear Bitcoin Community,

It is time for us to let Multibit go. 

KeepKey acquired Multibit a little over 1 year ago. At the time, the engineers who originally built and supported Multibit had announced that they would no longer be working on it or providing support. Multibit played an important role in the Bitcoin infrastructure. We felt that it was important for Multibit to continue and hoped that with our existing support and development teams, we would be able to keep Multibit alive.

The reality is that Multibit is in need of a lot of work. It has stubborn bugs that have caused us and Multibit users much grief. Additionally, Bitcoin has gone through a fundamental change in regards to the way fees work. The addition of SegWit in the coming weeks will mean the Multibit software has fallen still further behind.

Unfortunately, KeepKey simply does not have the resources to support the current issues, nor to rebuild Multibit to ensure ideal user experience. By focusing our attention on the KeepKey device, we will continue building and improving the best hardware wallet available.

Thus, KeepKey will discontinue support and maintenance of Multibit, effective immediately.

We recommend that all Multibit users discontinue using it and you move your keys to other wallet software of your choosing. 

## Next Steps for Multibit Users 
Videos that demonstrate how to move your wallet to Electrum are available on YouTube.

- Multibit HD: https://youtu.be/E-KcY6KUVnY
- Multibit Classic: https://youtu.be/LaijbTcxsv8

Please note that the version of Electrum available for download today (version 2.8.3) doesn’t fully support the importing Multibit HD wallet words. The version shown in the Multibit HD video is the soon-to-be-released next version.

Multibit was a fantastic piece of software in its time, and we want to thank the Multibit developers for such an important contribution to Bitcoin’s history.

Sincerely,

Ken Heutmaker

CTO, KeepKey 

------

Build status: [![Build Status](https://travis-ci.org/bitcoinj/bitcoinj.png?branch=master)](https://travis-ci.org/bitcoinj/bitcoinj)  
Coverage status: [![Coverage Status](https://coveralls.io/repos/bitcoinj/bitcoinj/badge.png?branch=master)](https://coveralls.io/r/bitcoinj/bitcoinj?branch=master)

### Welcome to bitcoinj

The bitcoinj library is a Java implementation of the Bitcoin protocol, which allows it to maintain a wallet and send/receive transactions without needing a local copy of Bitcoin Core. It comes with full documentation and some example apps showing how to use it.

### Technologies

* Java 6+
* [Maven 3+](http://maven.apache.org) - for building the project
* [Orchid](https://github.com/subgraph/Orchid) - for secure communications over [TOR](https://www.torproject.org)
* [Google Protocol Buffers](https://code.google.com/p/protobuf/) - for use with serialization and hardware communications

### Getting started

To get started, it is best to have the latest JDK and Maven installed. The HEAD of the `master` branch contains the latest development code and various production releases are provided on feature branches.

#### Building from the command line

To perform a full build use
```
mvn clean package
```
You can also run
```
mvn site:site
```
to generate a website with useful information like JavaDocs.

The outputs are under the `target` directory.

#### Building from an IDE

Alternatively, just import the project using your IDE. [IntelliJ](http://www.jetbrains.com/idea/download/) has Maven integration built-in and has a free Community Edition. Simply use `File | Import Project` and locate the `pom.xml` in the root of the cloned project source tree.

### Example applications

These are found in the `examples` module.

#### Forwarding service

This will download the block chain and eventually print a Bitcoin address that it has generated.

If you send coins to that address, it will forward them on to the address you specified.

```
  cd examples
  mvn exec:java -Dexec.mainClass=org.bitcoinj.examples.ForwardingService -Dexec.args="<insert a bitcoin address here>"
```

Note that this example app *does not use checkpointing*, so the initial chain sync will be pretty slow. You can make an app that starts up and does the initial sync much faster by including a checkpoints file; see the documentation for
more info on this technique.

### Where next?

Now you are ready to [follow the tutorial](https://bitcoinj.github.io/getting-started).
