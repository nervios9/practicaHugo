# What is Hugo
Hugo is a modern general purpose website creation framework. It falls into the category of new static site generators, based on the JAMstack dynamic architecture and written entirely in Go. It was originally created by Steve France in 2013.
# Facility
In this tutorial we are going to install Hugo

We are going to install it in its extended version, which includes its base program and some extra features that can come in handy
Installation Hugo on Linux
Check if we have Snap installed

To install Hugo on Linux we are going to use the Snap package manager. For this reason, the first thing we are going to do is check if we have this manager installed, for this we will use the following command:

```snap version
```


This should respond to us with the following message:

```snap 2.55.3+22.04
snapd 2.55.3+22.04
series 16
ubuntu 22.04
kernel 5.15.0-48-generic
```

In that case it will mean that we have snap installed. Then we can start with the installation.
Install the hugo-extended package

Using the Snap manager we are going to install the hugo-extended package.
```
snap install hugo --channel=extended
```
Installation Hugo on Windows

We will have to access Hugo's page and go to downloads.

Once here we will download the latest version that has a name of the format hugo_extended_x.x.x_windows-amd64.zip where x.x.x will correspond to the version.

This zip will contain the CMS, but the installation will have to be done manually.

We will extract the zip and for ease we will move the resulting Hugo.exe file to the path C:\Hugo\bin which we will create.

Once we have it, in the Windows search engine, we will access Edit system environment variables looking for this in it.

A window called System Properties will open and in this we will click on Environment variables again.

In the list that will show us we will look for the PATH variable, and at the end of it we will add ';C:\Hugo\bin'.

With this restarting the system we will have hugo installed and accessible in our system.
Installation Hugo on macOS

If we do not have it already installed, we will install the brew package manager with the following command

```ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
Once installed, we will use this command to install Hugo.
``` brew install hugo
```
Creation of the site with Hugo
Creating the site

Following the previous tutorial we should already have Hugo installed on our system.

Now to create a site with the CMS we will use the commands:
# WARNING THESE COMMANDS MUST BE CARRIED OUT FROM OUR USUAL USER, NEVER FROM SUDO

```hugo new site sitename
cd sitename
```
Our site is already created, but at the moment it is not functional. In order for this to work, we must first find a theme to use.
Installing a theme on the site

As an example I am going to use the PaperMod theme, but there are many on the internet that we can use. To install the theme what we will do in this case (each theme can have its own installation method, but most are this way)

```echo "theme = 'hugo-PaperMod'" >> config.toml
cd themes
#Clone or download in this folder the theme that we like.
git clone https://github.com/adityatelange/hugo-PaperMod
# We enter the folder of our theme
cd hugo-PaperMod
# We delete the .git folder from this theme so that it does not cause us problems
#when uploading our page
rm -rf .git
```
 

With this we will have the theme installed and we can start our site using

```hugo-server
```
After starting it, the command will return a URL in which we can see our site while this server is on.
Creating articles in Hugo

To create articles in Hugo we must go to the content folder, and inside the post folder we can start writing these in MarkDown or MD format for short.

As we write this it will be added to the site and visible on our local server.
Below I leave a link to a video to better understand how the installation is
{{<youtube tPP-P289BbY>}}