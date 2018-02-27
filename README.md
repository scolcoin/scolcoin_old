# scolcoin
Instructions install Deamon
$ sudo apt-get update 
$ sudo apt-get upgrade
Step 1. Create a user for running scolcoind
This step is optional, but for better security and resource separation I suggest you create a separate user just for running scolcoind . We will also use the ~/bin directory to keep locally installed files (others might want to use /usr/local/bin instead). We will download source code files to the ~/src directory.

$ sudo adduser scolcoin --disabled-password
$ sudo apt-get install git
$ sudo su - scolcoin
$ mkdir ~/bin ~/src
$ echo $PATH
If you don't see /home/scolcoin/bin in the output, you should add this line to your .bashrc, .profile, or .bash_profile, then logout and relogin:

PATH="$HOME/bin:$PATH"
$ exit
Step 2. Download scolcoind
We currently recommend scolcoind stable.

If you prefer to compile scolcoind, here are some pointers for Ubuntu:

$ sudo apt-get install build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev git libssl1.0.0-dbg
$ sudo apt-get install libdb-dev libdb++-dev libboost-all-dev libminiupnpc-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev
$ sudo su - scolcoin
$ cd ~/src 
$ mkdir scolcoin
$ cd scolcoin
$ wget http://scolcoin.com/descargas/scolcoin-source.tar.gz
$ tar -xzvf scolcoin-source.tar.gz
$ cd scolcoin/src
$ make -f makefile.unix RELEASE=1
$ strip scolcoind
$ cp -a scolcoind ~/bin
$ cd ~/bin

### Step 3. Configure and start icolcoind
In order to "talk" to scolcoind, we need to set up an RPC username and password for scolcoind. We will then start scolcoind and wait for it to complete downloading the blockchain.

$ mkdir ~/.scolcoin
$ nano ~/.scolcoin/scolcoin.conf
 # Use user and password
 rpcuser=rpc_scolcoin
 rpcpassword=69c863e3356d3dae95df454a1
 rpcallowip=127.0.0.1
 # Listening mode
 listen=1

 server=1
 txindex=1
 daemon=1
 # Use as many addnode=
 addnode=5.189.144.197
 addnode=80.241.214.59
 addnode= 173.249.23.32
Ctrl + x Y (Yes) (Enter)

start:

$ scolcoind
stop:

$ scolcoind stop
help:

$ scolcoind help 
Scolcoin development tree
