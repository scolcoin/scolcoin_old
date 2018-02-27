# scolcoin
Instructions install Deamon <br/>
$ sudo apt-get update  <br/>
$ sudo apt-get upgrade <br/>
<br/>
Step 1. Create a user for running scolcoind <br/>
This step is optional, but for better security and resource separation I suggest you create a separate user just for running scolcoind . We will also use the ~/bin directory to keep locally installed files (others might want to use /usr/local/bin instead). We will download source code files to the ~/src directory.
<br/><br/>
$ sudo adduser scolcoin --disabled-password <br/>
$ sudo apt-get install git <br/>
$ sudo su - scolcoin <br/>
$ mkdir ~/bin ~/src <br/>
$ echo $PATH <br/>
If you don't see /home/scolcoin/bin in the output, you should add this line to your .bashrc, .profile, or .bash_profile, then logout and relogin:
<br/>
PATH="$HOME/bin:$PATH" <br/>
$ exit <br/>
Step 2. Download scolcoind <br/>
We currently recommend scolcoind stable. <br/>
<br/>
If you prefer to compile scolcoind, here are some pointers for Ubuntu: <br/>
<br/>
$ sudo apt-get install build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev git libssl1.0.0-dbg <br/>
$ sudo apt-get install libdb-dev libdb++-dev libboost-all-dev libminiupnpc-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev <br/>
$ sudo su - scolcoin <br/>
$ cd ~/src  <br/>
$ mkdir scolcoin <br/>
$ cd scolcoin <br/>
$ wget http://scolcoin.com/descargas/scolcoin-source.tar.gz <br/>
$ tar -xzvf scolcoin-source.tar.gz <br/>
$ cd scolcoin/src <br/>
$ make -f makefile.unix RELEASE=1 <br/>
$ strip scolcoind <br/>
$ cp -a scolcoind ~/bin <br/>
$ cd ~/bin <br/>
<br/>
### Step 3. Configure and start icolcoind <br/>
In order to "talk" to scolcoind, we need to set up an RPC username and password for scolcoind. We will then start scolcoind and wait for it to complete downloading the blockchain. <br/>
<br/>
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
Ctrl + x Y (Yes) (Enter) <br/>
<br/><br/>
start: <br/>
 <br/>
$ scolcoind <br/>
stop: <br/>
 <br/>
$ scolcoind stop <br/>
help: <br/>
<br/>
$ scolcoind help <br/>
Scolcoin development tree <br/>
