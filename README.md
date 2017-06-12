# AmericanCoin - In Decentralization we trust


### Introduction

AmericanCoin is a private, secure, untraceable, decentralised digital currency. 
You are your bank, you control your funds, and nobody can trace your 
transfers unless you allow them to do so.

**Privacy**: AmericanCoin uses a cryptographically sound system to allow you to send and receive funds without your 
transactions being easily revealed on the blockchain (the ledger of transactions that everyone has). This ensures that your purchases, receipts, and all transfers remain absolutely private by default.

**Security**: Using the power of a distributed peer-to-peer consensus network, every transaction on the network is 
cryptographically secured. Individual wallets have a 25 word mnemonic seed that is only displayed once, and can be written down to backup the wallet. Wallet files are encrypted with a passphrase to ensure they are useless if stolen.

**Untraceability**: By taking advantage of ring signatures, a special property of a certain type of cryptography, AmericanCoin
 is able to ensure that transactions are not only untraceable, but have an optional measure of ambiguity that ensures that transactions cannot easily be tied back to an individual user or computer.
 
 
### About AmericanCoin

This is the core implementation of AmericanCoin. It is open source and completely free to use without restrictions, 
except for those specified in the license agreement below. There are no restrictions on anyone creating an 
alternative implementation of AmericanCoin that uses the protocol and network in a compatible manner.

As with many development projects, the repository on Github is considered to be the "staging" area for the latest changes. Before changes are merged into that branch on the main repository, they are tested by individual developers in their own branches, submitted as a pull request, and then subsequently tested by contributors who focus on testing and code reviews. That having been said, the repository should be carefully considered before using it in a production environment, unless there is a patch in the repository for a particular show-stopping issue you are experiencing. It is generally a better idea to use a tagged release for stability.

**Anyone is welcome to contribute to AmericanCoin's codebase!** If you have a fix or code change, feel free to submit
 it as a 
pull request directly to the "master" branch. In cases where the change is relatively small or does not affect other parts of the codebase it may be merged in immediately by any one of the collaborators. On the other hand, if the change is particularly large or complex, it is expected that it will be discussed at length either well in advance of the pull request being submitted, or even directly on the pull request.


# INSTALLATION AND USAGE:


You can download the executables directly from our servers or you can build them using your own computer.


## LINUX


### Downloading the Core

[Download for Linux](https://firebasestorage.googleapis.com/v0/b/americancoinintro.appspot.com/o/Linux%2FAMCCore.tar.gz?alt=media&token=47157757-06a1-4c46-af07-7f3dde63eb3e)

Extract the files by typing

```
tar -xzvf AMCCore.tar.gz
```

Once files have been extracted you can run a node by typing

```
./americancoind
```

If you're experiencing issues with permissions, use **chwon** or **chmod** to assign the executables the proper 
permissions.

You can solo-mine, generate a wallet address and more by running

```
./simplewallet
```

### Building AmericanCoin

In order to create your own build, firstly you must install all dependencies

```
sudo apt-get install build-essential git cmake libboost1.55-all-dev
```

Once everything has been installed, clone this repository
```
git clone https://github.com/AmericanCoinAMC/Core
```

Now you're ready to build the AmericanCoin Core
```
cd Core

make -j
```

Keep in mind that -j will use all your CPU threads, if you are building on low end hardware use **make** instead.


#### Creating a Service

If you wish to create a Service in order to run the AMC Core 24/7 we strongly suggest you start AMC's core as a 
service-daemon


```
description "AmericanCoin daemon"

start on runlevel [2345]
stop on runlevel [!2345]

respawn
respawn limit 10 5

pre-start script
	mkdir -p path/to/your/logfile
end script

exec path/to/the/daemon/amerciancoind --log-file path/to/your/logfile --no-console
```

**NOTE**

You can find all available options by typing
```
./americancoind --help
./simplewallet --help
```



## MAC OS X

**WARNING**

AMC's Core will only work in OS 10.9 & 10.11 & may not be compatible with PowerPc Macs.

**Note**

In order to run AMC Core & the Simple Wallet on Mac OS you will need Boost C++ libraries.

You can obtain these with 

Homebrew
```
brew install boost
```

or

MacPorts

```
port install boost
```

For more information visit:

Homebrew <http://docs.brew.sh/Installation.html>

MacPorts <https://guide.macports.org/#installing>

### Downloading the Core

[Download for Mac](https://firebasestorage.googleapis.com/v0/b/americancoinintro.appspot.com/o/Mac%2FAMCCore.zip?alt=media&token=397c6649-5076-4611-91c8-f1e28002ef5e)

Once you have extracted the files, open a terminal and locate yourself in the AMC's Core directory (Where americancoind is located). 

Then, simply type:

~~~
./americancoind 
~~~

## WINDOWS

[Download the Core for Windows](https://firebasestorage.googleapis.com/v0/b/americancoinintro.appspot.com/o/Mac%2FAMCCore.zip?alt=media&token=397c6649-5076-4611-91c8-f1e28002ef5e)

After extracting the files, locate yourself in that directory using the console and 
run:


 ```
 americancoin.exe 
 ```
 
 If you are interested in solo-mining using windows, we suggest you generate your wallet address using the [Wallet GUI](https://github.com/AmericanCoinAMC/Wallet)

 

### Licence

See [Licence](https://github.com/AmericanCoinAMC/Core/blob/master/LICENCE.txt)
 