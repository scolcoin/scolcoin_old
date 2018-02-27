Deamon
===========================

Instructions install Deamon <br/>
$ sudo apt-get update  <br/>
$ sudo apt-get upgrade <br/>
<br/>
Library: <br/>
$ sudo apt-get install build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev git libssl1.0.0-dbg  <br/>
$ sudo apt-get install libdb-dev libdb++-dev libboost-all-dev libminiupnpc-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev
<br/><br/>
$ mkdir scolcoin <br/>
$ cd scolcoin <br/>
$ wget http://scolcoin.com/descargas/scolcoin-daemon-linux.tar.gz <br/>
$ tar -xzvf scolcoin-daemon-linux.tar.gz <br/>
$ strip scolcoind <br/><br/>

$ mkdir ~/.scolcoin <br/>
$ nano ~/.scolcoin/scolcoin.conf <br/>
 rpcuser=rpc_scolcoin <br/>
 rpcpassword=69c863e3356d3dae95df454a1 <br/>
 rpcallowip=127.0.0.1 <br/>
 listen=1 <br/>
 server=1 <br/>
 txindex=1 <br/>
 daemon=1 <br/>
 addnode=5.189.144.197 <br/>
 addnode=80.241.214.59 <br/>
 addnode= 173.249.23.32 <br/>
Ctrl + x Y (Yes) (Enter) <br/><br/>

start: <br/><br/>

$ scolcoind

