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
sudo apt-get install build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev git libssl1.0.0-dbg <br/>
sudo apt-get install libdb-dev libdb++-dev libboost-all-dev libminiupnpc-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev
<br/>
Download the Scolcoin deamon file in a link or attach to the email and upload it using SCP / Filezilla. (Only available for paid customers)

# First step
sudo adduser scolcoin --disabled-password <br/>
Full Name []:  (enter) <br/>
        	Room Number []:(enter) <br/>
        	Work Phone []:(enter) <br/>
        	Home Phone []:(enter) <br/>
       	Other []:(enter) <br/>
sudo apt-get install git <br/>
sudo su - scolcoin <br/>
mkdir ~/bin ~/src <br/>
PATH="$HOME/bin:$PATH" <br/>
echo $PATH  <br/>
(/home/scolcoin/bin:…) I´m fine <br/>
cd src <br/>
wget http://scolcoin.com/descargas/scolcoin-daemon-linux.tar.gz <br/>
 <br/>
# Second step
Extract the tar file using the following command. <br/>
tar -xzvf scolcoin-daemon-linux.tar.gz <br/>

# Third step
strip scolcoind <br/>
cp -a scolcoind ~/bin <br/>
cd <br/>
cd bin <br/>
chmod +x scolcoind <br/>

# Fourth step

Create the configuration file. <br/>
mkdir ~/.scolcoin <br/>
nano ~/.scolcoin/scolcoin.conf <br/>

Paste the following lines in yourcoin.conf. <br/>
rpcuser=rpc_scolcoin <br/>
rpcpassword=69c863e3356d3dae95df454a1 <br/>
rpcallowip=127.0.0.1 <br/>
listen=1 <br/> 
server=1 <br/>
txindex=1 <br/>
daemon=1 <br/>
addnode=5.189.144.197 <br/>
addnode=80.241.214.59 <br/>
addnode= 173.249.23.32 <br/> <br/>

Store with the Ctrl + x key <br/>
Question do you want to store? press Y key (Yes) <br/>
Then Press key (Enter) <br/>
  <br/>
Start your node with the following command. <br/>
scolcoind <br/>

They will get the message "Scolcoin server starting" <br/>

It is already running if you want to turn it off you can put the command <br/>
scolcoind stop <br/>

if you want to see the current status of the network: <br/>
scolcoind getinfo <br/>

You will already have the server with the scolcoind configured. <br/>

Create in Tasks (Optional) <br/>
Log with root user and change the directory to /etc/init/. <br/>
$ cd /etc/init <br/>
Create the upstart config file. <br/>
$ cat > scolcoin-daemon.conf  <br/>

description "scolcoin daemon" <br/>

start on runlevel [23] <br/>
stop on shutdown <br/>

exec sudo -u fork /home/scolcoin/bin/scolcoind <br/>
post-stop exec sleep 30 <br/>

respawn <br/> 
respawn limit 5 30 <br/>


Start the service. <br/>
$ start scolcoin-daemon  <br/>

You now have your seed node up and running. It will automatically restart if something goes wrong. <br/>

Stopping the service. <br/>
$ stop scolcoin-daemon  <br/>
