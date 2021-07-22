### Introduction

Before we start learning, we'll need to install C# first. This section is where you could potentially encounter a lot of errors.

Before continuing, let's review a few best practices to keep in mind:

* Copy and paste the commands to avoid typos.
* Follow the directions closely, and don't skip over any sections.
* **Do NOT use `sudo` unless The Odin Project specifically says to do so.** Failing to follow this can cause a lot of headaches, and never run as the `root` user. In some instances, you might see a message in the terminal telling you to use sudo and install something with `apt`. Ignore that and follow _our_ instructions for now.

Now, let's get started!

<details markdown="block">
<summary class="dropDown-header">Ubuntu / Xubuntu</summary>

### Step 1: Install Updates, Packages and Libraries

Before we can install C#, we need to install some base packages.

#### Step 1.1: Open the Terminal

We'll use the terminal to install all of the programs.

If you're using Ubuntu or Xubuntu, simply press `Ctrl + Alt + T` to open the terminal. (This may work in other Linux distributions: you'll have to try!)

**Quick tip:** In Linux, you can copy from the terminal with `ctrl + shift + c` and paste with `ctrl + shift + v`.

#### Step 1.2: Update Linux

The rest of the installation will take place inside the terminal window.

First, we need to make sure your Linux distribution is up to date. Run these commands one by one. Because these commands use `sudo`, you will have to enter your password in order for them to run. When typing your password, you may not get any visual feedback, but rest assured that your password is being entered. Once you're done typing your password, press `enter`.

~~~bash
sudo apt update
sudo apt upgrade
~~~

When it prompts you, press `y` and then `enter`.

#### Step 1.3: Install the SDK

In order to use C#, we need to start installing the .NET SDK and Runtime. In this step, we will install the SDK.

First, we need to add Microsoft package signing to our list of trusted keys. Be sure to copy the following commands:

~~~bash
wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
rm packages-microsoft-prod.deb
~~~

With that done, we can now install the SDK:

~~~bash
sudo apt-get update; \
  sudo apt-get install -y apt-transport-https && \
  sudo apt-get update && \
  sudo apt-get install -y dotnet-sdk-5.0
~~~

#### Step 1.4: Install the runtime

Now that we have the SDK installed, we will install the runtime. This is sometimes **unnecessary**, but we will be running this command just to make sure the runtime is present on your machine:

~~~bash
sudo apt-get update; \
  sudo apt-get install -y apt-transport-https && \
  sudo apt-get update && \
  sudo apt-get install -y aspnetcore-runtime-5.0
~~~

#### Step 1.5: Completed!

Congratulations, you should now have the ability to write C# on your machine with the .NET 5 ecosystem!

</details>

<details markdown="block">
<summary class="dropDown-header">MacOS</summary>

### Step 1: Use the Official Installer

Getting C# installed on a Mac is super simple: just visit [download the .NET 5.0 installer for MacOS](https://download.visualstudio.microsoft.com/download/pr/6f2d055d-6092-4236-9824-b8326f971301/663c758102cacc0e3f4288c6462fac3f/dotnet-sdk-5.0.302-osx-x64.pkg
) and run it!

### Step 2: Install Heroku

Heroku is a place to host your Rails applications

#### Step 2.1: Install Heroku

Next, install Heroku:

~~~bash
brew install heroku/brew/heroku
~~~

This command will install the command line interface for Heroku, a free website that can host your Ruby on Rails applications. You'll learn more about this later.

</details>

#### Extras

If you are using Visual Studio Code as your text editor - which we assume for this course - you can install the "C#" extension which will provide you with lots of support for your code. Go to the "Extensions" tab in VSC (Ctrl+Shift+X), search "C#", and click install on the first one. Congratulations, the extension is now installed (you can also uninstall the extension from here).