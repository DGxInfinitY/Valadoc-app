# Valadoc-app
This is a Desktop Application for the Valadoc website buiild with nativefier and electron-forge

# Installation Instructions
Download the appropreate installer file in the releases tab for your computer. Then install the package.\
https://github.com/DGxInfinitY/Valadoc-app/releases

# Build Instructions
This will be updated periodically when new platforms are added.
### For Ubuntu Based Linux Distrobutions
#### Prerequisites
You must install:\
*npm*\
*electron-forge*\
*nativefier*\
*git-lfs*

```bash
sudo apt install npm -y
sudo npm install electron-forge -g
sudo npm install nativefier -g
```
Then you need to git clone. This project includes a large file that uses git-lfs to store. That means you may need to clone using the git-lfs tool to actually clone the whole project rather than most of the project and a pointer file in place of the large file. Once this has been completed successfully you will need to go into the folder

```bash
sudo apt install git-lfs -y
git-lfs clone https://github.com/DGxInfinitY/Valadoc-app.git
cd Valadoc-app
```
Then we need to essentially compile a system specific electron because we need a base electron to run and build the application from. This is accomplished by running a command while in the project folder:
```bash
npm install electron-prebuilt-compile --save-exact
```
This will then install the electron into the right place and you should then be able to develop and build the program on your hardware.

## Building
To build you can now simply run this command:
```bash
electron-forge make
```
And it will build the standard .deb (arch specific IE: If compiled on ARM64 the program will be built for ARM64 as a deb)
However the fun part comes in building for specific platforms and package types. You can build for Mac, Windows, and Linux in various formats. To configure this you simply need to edit the package.json file. Edit the part makers(Toward the end of the file)
For a list of avaliable configureations please see https://v6.electronforge.io/makers/

# TODO
Build a Windows Executable/installer\
Build a Mac Executable/installer\
Squash Bugs
