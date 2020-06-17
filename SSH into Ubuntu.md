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

## 5. Configure key based authentication

### 5.1 Create your local SSH key pair
```Shell
ssh-keygen -t rsa -b 4096
```

Notice: when asked to enter passphrase, just ignore it

### 5.2 Connecting to a macOS or Linux SSH host
```Shell
export USER_AT_HOST="your-user-name-on-host@hostname"
export PUBKEYPATH="$HOME/.ssh/id_rsa.pub"
ssh-copy-id -i "$PUBKEYPATH" "$USER_AT_HOST"
```

Notice: 1. USER_AT_HOST should be the id of the remote; 2. No need to change PUBKEYPATH



