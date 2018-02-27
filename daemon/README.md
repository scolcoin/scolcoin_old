Deamon
===========================

Instructions install Deamon
$ sudo apt-get update 
$ sudo apt-get upgrade

Library:
$ sudo apt-get install build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev git libssl1.0.0-dbg
$ sudo apt-get install libdb-dev libdb++-dev libboost-all-dev libminiupnpc-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev

$ mkdir scolcoin
$ cd scolcoin
$ wget http://scolcoin.com/descargas/scolcoin-daemon-linux.tar.gz
$ tar -xzvf scolcoin-daemon-linux.tar.gz
$ strip scolcoind

$ mkdir ~/.scolcoin
$ nano ~/.scolcoin/scolcoin.conf
 rpcuser=rpc_scolcoin
 rpcpassword=69c863e3356d3dae95df454a1
 rpcallowip=127.0.0.1
 listen=1
 server=1
 txindex=1
 daemon=1
 addnode=5.189.144.197
 addnode=80.241.214.59
 addnode= 173.249.23.32
Ctrl + x Y (Yes) (Enter)

start:

$ scolcoind

