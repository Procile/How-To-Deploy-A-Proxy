## Install Nodejs
If you haven't already install the latest version of Nodejs using this command :
```sh
curl -fsSL https://deb.nodesource.com/setup_current.x | sudo -E bash - &&\
```
then :
```sh
sudo apt-get install -y nodejs
```
verify you have the correct version of nodejs :
```sh
node -v
```
Output :
```sh
V19.6.0
```
verify you have the correct version of npm :
```sh
npm -v
```
Output :
```sh
9.4.0
```
## Install Git
If you haven't already install Git
```sh
sudo apt install git
```
## Cloning
Cloning ThingsWeb is as simple as running `git clone`, and then the link to the repository :
```sh
sudo git clone https://github.com/Darkness-Organization/Neb
```
## Installing Dependencies
Go inside the CD :
```sh
cd Neb/
```
Install npm :
```sh
npm i
```
## Starting the Site
See the command below:
```sh
$ npm start
```
