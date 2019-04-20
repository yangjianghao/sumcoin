
# Sumcoin is NOT an OPEN Source Coin
If you have questions and wish to license, you should contact us at the email below for commercial uses

### !! NOTICE TO ANY EXCHANGE OR DEVELOPERS ETC -  THIS COIN IS INDEX BASED AND YOU SHOULD CONTACT US WITH QUESTIONS!!

OBJECT IS **INDEX BASED**, ALGO BASED COIN FOR USE IN **ATM'S** 

### See General Bytes Twitter for example:
https://twitter.com/generalbytes/status/1098174237163077633

FOR QUESTIONS, AUTHORIZATIONS, CONTACT : ATTN DEVS @ Support@SumcoinIndex.com

### BATM Setup instructions:
https://github.com/sumcoinlabs/sumcoin/wiki/Sumcoin-Core-(sumcoind)-BATM-Configuration

//---

## Sumcoin integration/staging tree

CONTACT US: Support@SumcoinIndex.com Twitter https://twitter.com/SumCoinIndex Facebook @SumCoinIndex

Main Website https://SumcoinIndex.com

### Email 
Support@SumcoinIndex.com



# Mining

Mining Pool Website http://sumcoinpool.org

## Stratum connect info 
stratum+tcp://sumcoinpool.org:3340

Pricing Info http://sumcoinprice.com/

SUM Block Explorer http://sumexplorer.com

TODO - Add charts from db to sumcoinprice.com

Download versions & other Information: http://Sumcoin.cash

## PRICE Data

Exchange rate Pricing JSON API : 

### Integer, Rate, Symbol :

https://sumcoinindex.com/rates/price.json

AND

### Last buy, last price, last sell rate data
https://sumcoinindex.com/rates/price2.json



# To Buy, Sell or Trade (Coin to Coin)
HTTPS://SumcoinTrade.com 


## Mining Hardware

### Sumcoin Algo is Scrypt

CPU, GPU Use CPU Miner by Pooler (see our link to cpu miner - minerd - in releases)

AMD GPU Cards SGMINER for AMD Cards : https://bit.ly/2k6zchT

Moonlander 2 USB Asic Miner : https://www.futurebit.io/


Copyright (c) 2009-2014 Bitcoin Developers Copyright (c) 2011-2017 Litecoin Developers Copyright (c) 2017-2018 Sumcoin Developers Copyright  (c) 2017-2019 Crypto Cloud Inc (c) 2017-2019 Sigma Systems Inc

## What is Sumcoin?

Sumcoin is a cryptographic blockchain using scrypt proof-of-work algorithm. Sumcoin tracks all coins in real time and is an aggregate or "sum" of all top 100 coins by market capitalization. It is for those who want to gain maximum exposure to the crypto space but may only want to hold one coin for simplicity, which can reduce risk factors.

## Times:

0.5 Min block targets

subsidy halves in 420 K blocks (~5 Months)

~100 million total coins

Initial reward
100 coins per block

720 blocks to retarget difficulty

For more information, as well as an immediately useable, binary version of the Sumcoin client sofware, see https://github.com/sumcoinlabs/sumcoin/releases

### License

Sumcoin is released under the terms of Classic Proprietary License. See COPYING for more information or see https://en.wikipedia.org/wiki/Proprietary_software.

### Development process

Developers work in their own trees, then submit pull requests when they think their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Sumcoin development team members simply pulls it.

If it is a more complicated or potentially controversial change, then the patch submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing. Developers should expect to rework and resubmit patches if the code doesn't match the project's coding conventions (see doc/coding.txt) or are controversial.

The master branch is regularly built and tested, but is not guaranteed to be completely stable. Tags are created regularly to indicate new official, stable release versions of Sumcoin.

### Linux Build Dependencies/instructions: (Also see Sumcoin Wiki for the same info)
 
Dependencies:
```
sudo apt-get update;
 
sudo apt-get install git;
 
sudo apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils;
 
sudo apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev;
 
sudo apt-get install -y libboost-all-dev;
 
sudo apt-get install -y software-properties-common
```
```
sudo add-apt-repository ppa:bitcoin/bitcoin
```
```
sudo apt-get update;
 
sudo apt-get install -y libdb4.8-dev libdb4.8++-dev;
 
sudo apt-get install -y libminiupnpc-dev;
 
sudo apt-get install -y libzmq3-dev;
 
sudo apt-get install -y libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler;
 
sudo apt-get install -y libqt4-dev libprotobuf-dev protobuf-compiler

### Next, Clone the project
``` 
git clone https://github.com/sumcoinlabs/sumcoin.git
```
### Change directories into Sumcoin
```
cd sumcoin
```
### From the Sumcoin Directory, run each command
```
./autogen.sh
```
Next,
```
./configure
```
or
```
./configure --disable-test
```
or
```
./configure --disable-tests --without-gui
```

## SPECIAL NOTE if using only 1 GB RAM - File Swap info (if needed):

Create swapfile using:
```
sudo fallocate -l 2G /swapfile
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
```
To turn off after you 'make'
```
sudo swapoff /swapfile
```

# Make

Last, make the executables
```
make
```

*It will then start compiling and take a while.*

### *IF you needed swapfile - BE sure to turn it off again:*

When it is done, turn off the swapfile with:
```
sudo swapoff /swapfile
```
### Run: 

After this it's ready to run. The executable will be in sumcoin/src. Run with:
```
./sumcoind -server -daemon
```
## Setup a configuration file to run as a node

Stop the server from sumcoin/src:
```
./sumcoin-cli stop
```
Navigate to sumcoin data dir from home dir
```
cd .sumcoin
```
```
touch sumcoin.conf
nano sumcoin.conf
```
Paste the following **make your own user/password***
```
server=1
daemon=1
rpcuser=user
rpcpassword=password
```

Restart Sumcoin.   You will now be running as a node each time you start
```
cd sumcoin/src
./sumcoind -server -daemon
```

**With GUI** - Not for Linux terminal
/sumcoin/src/qt/:./sumcoin-qt


## Configure your settings

1. navigate to hidden folders
2. create sumcoin.conf file
3. inside, set the following parameters from the list below

//TODO

### Testing

Testing and code review is the bottleneck for development; we get more pull requests than we can review and test. Please be patient and help out, and remember this is a security-critical project where any mistake might cost people lots of money.

Automated Testing
Developers are strongly encouraged to write unit tests for new code, and to submit new unit tests for old code.

Unit tests for the core code are in src/test/. To compile and run them:

cd src; make -f makefile.unix test
Unit tests for the GUI code are in src/qt/test/. To compile and run them:

qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
make -f Makefile.test
./sumcoin-qt_test
