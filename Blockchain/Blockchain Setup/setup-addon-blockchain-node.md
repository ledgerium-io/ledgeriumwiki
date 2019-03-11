# Setup blockchain "addon" node on a fresh linux machine

The blockchain ecosystem is a combination of multiple technologies that come together. It is overwhelming to know that so much has been achieved in a short span. The tech stacks range from (not limited to this list) GoLang, NodeJs, Haskell, Metamask, Solidity and supporting Web3 technologies. Hence this will always remain as a living document for the team.

## Install Docker CE

### SET UP THE REPOSITORY

Reference: https://docs.docker.com/install/linux/docker-ce/ubuntu/

1. Update the `apt` package index:
```
$ sudo apt-get update
```

2. Install packages to allow `apt` to use a repository over HTTPS:

```
$ sudo apt-get install \
apt-transport-https \
ca-certificates \
curl software-properties-common
```

3. Add Docker’s official GPG key:
```
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
should return OK


```
$ sudo apt-key fingerprint 0EBFCD88

pub   4096R/0EBFCD88 2017-02-22
      Key fingerprint = 9DC8 5822 9FC7 DD38 854A  E2D8 8D81 803C 0EBF CD88
uid                  Docker Release (CE deb) <docker@docker.com>
sub   4096R/F273FCD8 2017-02-22
```

4. Use the following command to set up the stable repository. You always need the stable repository, even if you want to install builds from the edge or test repositories as well. To add the edge or test repository, add the word edge or test (or both) after the word stable in the commands below.


```
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" sudo apt-get update
```

```
Note: The lsb_release -cs sub-command below returns the name of your Ubuntu distribution, such as xenial. Sometimes, in a distribution like Linux Mint, you might need to change $(lsb_release -cs) to your parent Ubuntu distribution. For example, if you are using Linux Mint Rafaela, you could use trusty.
```

### Install Docker CE

1. Update the apt package index.

```
$ sudo apt-get update
```

2. Install the latest version of Docker CE, or go to the next step to install a specific version:
```
$ sudo apt-get install docker-ce
```

3. Verify that Docker CE is installed correctly by running the `hello-world` image.
```
$ sudo docker run hello-world
```

### Install Docker Compose

Reference : https://docs.docker.com/compose/install/

1. Run this command to download the latest version of Docker Compose:

```
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
```
Note : Install Docker Engine version 1.7.1 or greater: ...
```
2. Apply executable permissions to the binary:
```
$ chmod +x /usr/local/bin/docker-compose.
```
> 1. Optionally, install command completion for the bash and zsh shell.
> 2. Test the installation by docker-compose
> ```    
> $ docker-compose --version
> docker-compose version 1.23.2, build 1110ad01
> ```

#### To create the docker group and add your user:

1. Create the docker group.
```
$ sudo groupadd docker
```

2. Add your user to the docker group.

```
$ sudo usermod -aG docker $USER
```

3.  Log out and log back in so that your group membership is re-evaluated.

> If testing on a virtual machine, it may be necessary to restart the virtual machine for changes to take effect.

> On a desktop Linux environment such as X Windows, log out of your session completely and then log back in.

4. Verify that you can run docker commands without sudo .
```
$ docker run hello-world
```

## Install NodeJS
Reference:  https://linuxize.com/post/how-to-install-node-js-on-ubuntu-18.04/

```
sudo apt-get update &&
sudo apt-get -y upgrade &&
curl -sL https://deb.nodesource.com/setup_8.x -o nodesource_setup.sh &&
sudo bash nodesource_setup.sh &&
sudo apt-get install nodejs &&
rm nodesource_setup.sh
```

## Blockchain “addon” Node setup

### 1. Clone Ledgerium network
This repo contains externalised genesis and static-nodes files which will be created after "full" node setup.

```
mkdir ledgerium
cd ledgerium
git clone http://github.com/ledgerium/ledgeriumnetwork.git
```

### 2. Clone Ledgerium tools
Ledgerium tools is used to create a docker-compose.yml file
```
git clone http://github.com/ledgerium/ledgeriumtools.git
cd ledgeriumtools
npm install
```

Update initialparams.json file :
```
vi initialparams.json
```
Change `modeType = addon`, `nodeName = $(hostname)` and `domainName`


Note:
* User has to edit these values in the json file before running ledgerium tools application
* `domainName` is `optional` for `addon` mode

### 3. Create a docker network
```
docker network create -d bridge --subnet 172.19.240.0/24 --gateway 172.19.240.1 test_net
```

### 4. Run Ledgerium tools application

Before starting the addon node, create a directory /output/tmp in ledgerium tools and copy the externalised genesis and static-nodes files from ledgerium network to ‘tmp’ folder
```
cp ../ledgeriumnetwork/* ./output/tmp/
```

Run ledgerium tools application
```
node index.js
```

docker-compose will be generated in output folder

```
cd output
sudo docker-compose up -d
```

### 5. Check application status

Check the ./logs/constellationLogs and ./logs/gethLogs folders are created.
* `docker ps -a` shows list of containers mentioned below

    * Quorum node, governance_app_ui and constellation for each node
    * Quorum maker
    * Eth-stats
* Running `geth attach` command will work for quorum nodes.
