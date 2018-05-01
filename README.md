
Scolcoin development tree

Scolcoin is a PoS-based cryptocurrency.

Development process
===========================

Developers work in their own trees, then submit pull requests when
they think their feature or bug fix is ready.

The patch will be accepted if there is broad consensus that it is a
good thing.  Developers should expect to rework and resubmit patches
if they don't match the project's coding conventions (see coding.txt)
or are controversial.

The master branch is regularly built and tested, but is not guaranteed
to be completely stable. Tags are regularly created to indicate new
stable release versions of Scolcoin.

Feature branches are created when there are major new features being
worked on by several people.

From time to time a pull request will become outdated. If this occurs, and
the pull is no longer automatically mergeable; a comment on the pull will
be used to issue a warning of closure. The pull will be closed 15 days
after the warning if action is not taken by the author. Pull requests closed
in this manner will have their corresponding issue labeled 'stagnant'.

Issues with no commits will be given a similar warning, and closed after
15 days from their last activity. Issues closed in this manner will be 
labeled 'stale'.


MANUAL NODOS PIONEROS
===========================
¿Cómo crear un Nodo? (Scolcoin)
Características físicas de un Servidor Nodo:
•	Sistema Operativo Recomendado Linux Ubunto 14.10
•	CPU: two cores
•	6 GB RAM (guaranteed)
•	500 GB disk space (SSD-boosted)
•	SSD boost

Que es un Nodo?
===========================

Un nodo distribuye tu blockchain entre las personas que usan tu blockchain. 
La segunda característica de un nodo es que verifica las transacciones de tu blockchain.

¿Cómo me conecto con un nodo?
Puede conectarse manualmente a un nodo usando las siguientes instrucciones desde su wallet.

1.	Cierre su billetera y modifique el archivo scolcoin.conf en la carpeta "% APPDATA% \ scolcoin \".
2.	Pegue el siguiente texto en el archivo scolcoin.conf y guarde el archivo.

addnode=REPLACE_WITH_YOUR_IP_OR_HOSTNAME

Reemplace el texto "REPLACE_WITH_YOUR_IP_OR_HOSTNAME" con una dirección IP o nombre de host. 

Ejem addnode=37.97.242.80 o addnode=nodo1.scolcoin.com
No es necesario que ejecute un nodo alojado en nuestro hardware. 
Puede configurar un nodo en su propio VPS usando las siguientes instrucciones:
¿Cómo configuro un nodo en el servidor Ubuntu?
Puede configurar un nodo en su propio Ubuntu VPS usando las siguientes instrucciones.

Alquile un VPS que ejecute el servidor Ubuntu 14.04.
===========================

Actualiza tu VPS usando los siguientes comandos.
===========================

sudo apt-get update

sudo apt-get upgrade



Instale las dependencias necesarias usando los siguientes comandos.
===========================

sudo apt-get install build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev git libssl1.0.0-dbg

sudo apt-get install libdb-dev libdb++-dev libboost-all-dev libminiupnpc-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev

Descarga el archivo deamon de Scolcoin en un link o adjunto al correo y súbelo usando SCP / Filezilla. (Solo disponible para clientes pagados)

Primer Paso
===========================

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
(/home/scolcoin/bin:…) quedo bien
cd src
wget http://scolcoin.com/descargas/scolcoin-daemon-linux.tar.gz


Segundo Paso
===========================

Extraiga el archivo tar usando el siguiente comando.

tar -xzvf scolcoin-daemon-linux.tar.gz

Tercer Paso
===========================

strip scolcoind
cp -a scolcoind ~/bin
cd
cd bin
chmod +x scolcoind

Cuarto Paso
===========================

Crea el archivo de configuración.
mkdir ~/.scolcoin
nano ~/.scolcoin/scolcoin.conf


Pegue las siguientes líneas en yourcoin.conf.
===========================
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

Almacenar con la tecla Ctrl + x
Pregunta desea almacenar? oprima tecla  Y (Yes)
Luego Presione tecla (Enter)

Comience su nodo con el siguiente comando.
===========================
scolcoind

Les saldrá el mensaje “Scolcoin server starting”

Ya queda ejecutando si deseas apagarlo le pueden poner el comando

scolcoind stop

si deseas mas opciones pueden usar la función help

scolcoind help

si desean ver el estado actual de la red:

scolcoind getinfo

Ya tendras el servidor con el scolcoind configurado.
