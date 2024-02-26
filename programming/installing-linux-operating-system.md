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