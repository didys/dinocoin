DinoCoin Core (fork DINOCOIN) integration/staging repository
======================================


It is recommended [use the shell script](https://github.com/didys/lpcinstall) to install a DinoCoin Masternode on a Linux server running Ubuntu 14.04 or 16.04

***

Quick installation of the DinoCoin daemon under linux. See detailed instructions there [build-unix.md](build-unix.md)

Installation of libraries (using root user):

    add-apt-repository ppa:bitcoin/bitcoin -y
    apt-get update
    apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
    apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
    apt-get install -y libdb4.8-dev libdb4.8++-dev

Cloning the repository and compiling (use any user with the sudo group):

    cd
    git clone https://github.com/didys/DinoCoin.git
    cd DinoCoin
    ./autogen.sh
    ./configure
    sudo make install
    cd src
    sudo strip dinocoind
    sudo strip dinocoin-cli
    sudo strip dinocoin-tx
    cd ..

Running the daemon:

    dinocoind 

Stopping the daemon:

    dinocoin-cli stop

Demon status:

    dinocoin-cli getinfo
    dinocoin-cli mnsync status

All binaries for different operating systems, you can download in the releases repository:

https://github.com/didys/DinoCoin/releases

P2P port: 29997, RPC port: 29998
-
Distributed under the MIT software license, see the accompanying file COPYING or http://www.opensource.org/licenses/mit-license.php.
