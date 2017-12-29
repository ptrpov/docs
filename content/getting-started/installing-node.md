<!--
title: 02 - How to install npm & manage npm versions 
-->

#How to Install npm & Manage npm Versions

npm is written in Node.js, so your system needs to have Node.js before you can use npm. However, the two products are managed by different entities, so updates and maintenance can become complex. Also, the Node.js installation process installs npm in a directory that doesn't have global permissions. This can cause permissions errors when you attempt to run packages globally. 

To solve both these issues, npm recommends that you use a *node version manager*, or *nvm*, to install npm. The version manager will avoid permissions errors, and will solve the complexities of updating Node.js and npm. 

In addition, many developers like to test their applications on multiple versions of npm. Using a version manager makes it easy to switch versions.

##Installing npm with a Version Manager 

A version manager allows you to switch between node and npm versions, which makes it easier to ensure that your applications work for most users. Use the instructions for the version manager you select to learn how to switch versions, and to learn how to keep up-to-date with the latest version of npm. 

###Apple macOS 

There are several approaches for installing npm for the MacOS. 

####Installing NVM Directly

If you don't want to install Homebrew, click [here](https://github.com/creationix/nvm/blob/master/README.md#installation) to learn how to install nvm without it. 

###Using HomeBrew to Install node.js, npm, and nvm 

While the nvm readme file advises against installing nvm with HomeBrew, many Macintosh developers use [Homebrew](https://brew.sh/) along with nvm, and find the comnbination valuable. Homebrew is a Macintsoh tool that managing apps and files, a package manager for Macintosh. 

####Using HomeBrew to Install Node.js and npm

1. To install Homebrew, click [here](https://docs.brew.sh/Installation.html).

2. After you've installed Homebrew, run `brew install node` 

3. Homebrew will install Node.js and npm. 

4. To test successful installation of node, type `node -v`.

5. To test successful installation of npm, type `npm -v` 

At this point, npm has been installed in a location that will not lead to permssions errors. 

####Using HomeBrew to install a Node Version Manager

You can manually check for new versions from time to time, or you can install nvm, a Node Version Manager, using Homebrew. However, please read the instructions here before you begin. The nvm readme page advises against using HomeBrew to install nvm, so avoid doing this unless you are comfortable with the steps described. 

`brew install nvm`

`brew info nvm`

Follow the caveats that appear on the screen to ensure nvm is in the correct file location/path. Note: These caveats may differ depending on your configuration.

```
Add the following to $HOME/.bashrc, $HOME/.zshrc, or your shell's equivalent configuration file:

source $(brew --prefix nvm)/nvm.sh

Node installs will be lost when you upgrade nvm. Add the following about fhe sourc line to move install lcoation and prevent this:

export NVM_DIR=~/.nvm

```

Then, apply the changes by running the script. For example:

`Run .~/.bash)profile` 

to apply the changes you made to your .bash_profile file. 

###Microsoft Windows
 
To install and manage npm and Node.js on Windows, we recommend that you install this version manager, [nvm-windows](https://github.com/coreybutler/nvm-windows).

###Linux

Click [here] (https://github.com/creationix/nvm/blob/master/README.md#installation) to learn how to install nvm for Linux.

#Installing npm Directly

Although it is not recommended for most users, you can install npm without a version manager. The Nodejs.org installation process will install Node.js and npm into /usr/local. 

> Note: using this method to install npm can lead to permissions errors such as `EACCESS`. To learn more about permissions, see [Chapter 3](https://docs.npmjs.com/getting-started/fixing-npm-permissions).

###1. Install Node.js 

If you're using OS X or Windows, another way to install Node.js is to use one of the installers from the [Node.js download page](https://nodejs.org/en/download/). Be sure to install the version labeled **LTS**. Other versions have not been tested with npm. 
	
If you're using Linux, you can use the installer, or you can check [NodeSource's binary distributions](https://github.com/nodesource/distributions) to see whether or not there's a more recent version that works with your system.
	
After installing, run `node -v`. The version should be higher than v8.9.1

### 2. Update npm

Node comes with npm installed so you should have a version of npm. 
However, npm gets updated more frequently than Node does, so you'll want to make sure it's the latest version.

To test,  run `npm -v`. Compare this version with the version at the bottom of each page of doc (scroll down) to see if it's the latest version.

If the version is not the latest version, run:

`npm install npm@latest -g`

## How to Install npm from a Module

*For more advanced users*

The npm module is available for download on our [website](https://registry.npmjs.org/npm/-/npm-{VERSION}.tgz).

# Experimenting with the Next Release 

*For more advanced users*

If you want to try the next, unreleased version of npm to test packages you have created, use this command:

`npm install npm@next -g`

This may simply reinstall the current version, depending on the development cycle. 

## Learn More

To learn how to use nvm, click [here](https://github.com/creationix/nvm/blob/master/README.md#usage).

To learn how to troubleshoot HomeBrew/npm/node installation, visit this [discussion](https://www.dyclassroom.com/howto-mac/how-to-install-nodejs-and-npm-on-mac-using-homebrew).

