# Installing Linux Operating system

In this documentation, I am writing to brain dump the things each time I do installation.\


### My preffered OS

#### &#x20;I usually prefer to install debian. I prefer to install debian because of it's stability, people I know and the core philosophy of the project. That's why I install it.



I have two free bootware USB sticks. With this it's pretty easy to install anything. The first one was gifted by Abhijit P A, Debian Developer and second one I got it during Debconf.



### Add user to sudoers

Edit: /etc/sudoers\
\
Add username in that file as:\
\


```
username ALL=(ALL) ALL
```

{% embed url="https://askubuntu.com/questions/7477/how-can-i-add-a-user-as-a-new-sudoer-using-the-command-line" %}

### Basic Installation software



```
sudo do apt update
sudo apt upgrade

sudo apt install wget
sudo apt install git

# Installation of chrome

wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install ./google-chrome-stable_current_amd64.deb
```



{% embed url="https://itsfoss.com/install-chrome-debian-kali-linux/" %}



### Text Editors



```
sudo apt install vim
```

Cursor.so and VSCODE



{% embed url="https://cursor.sh/" %}

{% embed url="https://code.visualstudio.com/docs/setup/linux" %}



```
apt install ./<>.deb

#older version
sudo dpkg -i <file>.deb
# sudo apt-get install -f # Install dependencies
```



Configurations:

{% embed url="https://raw.githubusercontent.com/kurianbenoy/reimagined-dotfiles/master/.vimrc" %}



{% embed url="https://raw.githubusercontent.com/kurianbenoy/reimagined-dotfiles/master/.bash_aliases" %}

{% embed url="https://github.com/kurianbenoy/reimagined-dotfiles" %}



### Install nodejs



```
 sudo apt install nodejs npm
```

{% embed url="https://www.rosehosting.com/blog/how-to-install-node-js-and-npm-on-debian-11/" %}

### Install Python



```
wget https://raw.githubusercontent.com/fastai/fastsetup/master/setup-conda.sh

source setup-conda.sh
. ~/.bashrc
conda install -yq mamba -c conda-forge
```

{% embed url="https://kurianbenoy.com/posts/2022/2022-05-28-fastai-walthrus1.html" %}



### Settings



> Check mouse trackpad setting to enable double tap



### Displays in Linux

\
For screensharing\


Using two monitors?
