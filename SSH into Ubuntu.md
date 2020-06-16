# Tutorial for SSH into Ubuntu from Mac

## 1. First you need to enable the SSH on Ubuntu machine

```Shell
sudo apt update
sudo apt install openssh-server
```

## 2. Then to check whether ssh is successfully installed, run the following scripts:

```Shell
sudo systemctl status ssh
```

and the window should show ![ubuntu-ssh-status](https://github.com/ZhihaoZhu/Tips/blob/master/Images/ubuntu%20ssh%20tips/ubuntu-ssh-status.jpg?raw=true)

## 3. Ubuntu comes with a firewall configuration tool called UFW. If the firewall is enabled on your system, make sure to open the SSH port:

```Shell
sudo ufw allow ssh
```

## 4. Connecting to remote via ssh

```Shell
ssh username@ip_address
```
