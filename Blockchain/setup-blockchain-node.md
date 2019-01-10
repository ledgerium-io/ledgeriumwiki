# Setup blockchain "addon" node on a fresh linux machine

The blockchain ecosystem is a combination of multiple technologies that come together. It is overwhelming to know that so much has been achieved in a short span. The tech stacks range from  (not limited to this list) GoLang, NodeJs, Haskell, Metamask, Solidity and supporting Web3 technologies. Hence this will always remain as a living document for the team.


//Docker Installation 
Take formatting text from https://docs.docker.com/install/linux/docker-ce/ubuntu/ 

Install Docker CE
SET UP THE REPOSITORY
sudo apt-get update

sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common
Add Docker’s official GPG key:
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - should return OK

sudo apt-key fingerprint Check “9DC8 5822 9FC7 DD38 854A  E2D8 8D81 803C 0EBF CD88” /etc/apt/trusted.gpg
--------------------
pub   rsa4096 2017-02-22 [SCEA]
      9DC8 5822 9FC7 DD38 854A  E2D8 8D81 803C 0EBF CD88
uid           [ unknown] Docker Release (CE deb) <docker@docker.com>
sub   rsa4096 2017-02-22 [S]

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt-get update

apt-get install docker-ce

sudo docker run hello-world

Install Docker Compose .. https://docs.docker.com/compose/install/ 
Install Docker Engine version 1.7.1 or greater: ...
sudo curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

Apply executable permissions to the binary: $ chmod +x /usr/local/bin/docker-compose.
Optionally, install command completion for the bash and zsh shell.
Test the installation by docker-compose


//Docker Compose installation

chmod +x /usr/local/bin/docker-compose
Docker-compose command should work

To create the docker group and add your user:
Create the docker group. $ sudo groupadd docker.
Add your user to the docker group. $ sudo usermod -aG docker $USER.
Log out and log back in so that your group membership is re-evaluated. ...
Verify that you can run docker commands without sudo .


Install node from https://linuxize.com/post/how-to-install-node-js-on-ubuntu-18.04/ 

sudo apt-get update && sudo apt-get -y upgrade
curl -sL https://deb.nodesource.com/setup_11.x | sudo -E bash -
sudo apt-get install -y nodejs



Blockchain “addon” Node setup - To be script 

mkdir ledgerium
cd ledgerium/
git clone http://github.com/ledgerium/ledgeriumnetwork.git 

git clone http://github.com/ledgerium/ledgeriumtools.git
cd ledgeriumtools/
npm install
vi initialparams.json
//change modeType = ‘addon’
//nodeName = $(hostname)
docker network create -d bridge --subnet 172.19.240.0/24 --gateway 172.19.240.1 test_net

node index.js
//Copy the externalised genesis and static-nodes files to ‘tmp’ folder
cp ../ledgeriumnetwork/* ./outputs/tmp/
cd output
docker-compose ps -a

//Check 
the ./logs/constellationLogs and  ./logs/gethLogs folders are created
‘docker ps -a’ shows 3 containers running
Geth attach command work












