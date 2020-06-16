# Tutorial for SSH into Ubuntu from Mac

## First you need to enable the SSH on Ubuntu machine

```Shell
sudo apt update
sudo apt install openssh-server
```

## Then to check whether ssh is successfully installed, run the following scripts:

```Shell
sudo systemctl status ssh
```

and the window should show ![ubuntu-ssh-status](/Images/ubuntu ssh tips/ubuntu-ssh-status.jpg)
