Nodes Scolcoin
===========================

# How to create a Node? (Scolcoin)
Physical characteristics of a Node Server:
• Operating System Recommended Linux Ubunto 14.10
• CPU: two cores
• 6 GB RAM (guaranteed)
• 500 GB disk space (SSD-boosted)
• SSD boost

# What is a Node?

A node distributes your blockchain among the people who use your blockchain.
The second characteristic of a node is that it verifies the transactions of your blockchain.

# How do I connect with a node?
You can manually connect to a node using the following instructions from your wallet.

1. Close your wallet and modify the file scolcoin.conf in the folder "% APPDATA% \ scolcoin \".
2. Paste the following text in the scolcoin.conf file and save the file.

addnode = REPLACE_WITH_YOUR_IP_OR_HOSTNAME

Replace the text "REPLACE_WITH_YOUR_IP_OR_HOSTNAME" with an IP address or host name.
Example:  addnode = 37.97.242.80 or addnode = node1.scolcoin.com
It is not necessary to run a node hosted on our hardware.
You can configure a node in your own VPS using the following instructions:
How do I configure a node on the Ubuntu server?
You can configure a node in your own Ubuntu VPS using the following instructions.

Rent a VPS that runs the Ubuntu 14.04 server.

# Update your VPS using the following commands.
sudo apt-get update
sudo apt-get upgrade

# Install the necessary dependencies using the following commands.
sudo apt-get install build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev git libssl1.0.0-dbg
sudo apt-get install libdb-dev libdb++-dev libboost-all-dev libminiupnpc-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev

Download the Scolcoin deamon file in a link or attach to the email and upload it using SCP / Filezilla. (Only available for paid customers)

# First step
sudo adduser scolcoin --disabled-password
Full Name []:  (enter)
        	Room Number []:(enter)
        	Work Phone []:(enter)
        	Home Phone []:(enter)
       	Other []:(enter)
sudo apt-get install git
sudo su - scolcoin
mkdir ~/bin ~/src
PATH="$HOME/bin:$PATH"
echo $PATH 
(/home/scolcoin/bin:…) I´m fine
cd src
wget http://scolcoin.com/descargas/scolcoin-daemon-linux.tar.gz

# Second step

Extract the tar file using the following command.
tar -xzvf scolcoin-daemon-linux.tar.gz

# Third step
strip scolcoind
cp -a scolcoind ~/bin
cd
cd bin
chmod +x scolcoind

# Fourth step

Create the configuration file.
mkdir ~/.scolcoin
nano ~/.scolcoin/scolcoin.conf

Paste the following lines in yourcoin.conf.
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

Store with the Ctrl + x key
Question do you want to store? press Y key (Yes)
Then Press key (Enter)

Start your node with the following command.
scolcoind

They will get the message "Scolcoin server starting"

It is already running if you want to turn it off you can put the command
scolcoind stop

if you want to see the current status of the network:
scolcoind getinfo

You will already have the server with the scolcoind configured.

Create in Tasks (Optional)
Log with root user and change the directory to /etc/init/.
$ cd /etc/init
Create the upstart config file.
$ cat > scolcoin-daemon.conf 

description "scolcoin daemon"

start on runlevel [23]
stop on shutdown

exec sudo -u fork /home/scolcoin/bin/scolcoind
post-stop exec sleep 30

respawn
respawn limit 5 30


Start the service.
$ start scolcoin-daemon 

You now have your seed node up and running. It will automatically restart if something goes wrong.

Stopping the service.
$ stop scolcoin-daemon 
