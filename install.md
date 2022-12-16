</p>
<p style="font-size:14px" align="right">
<a href="https://discord.gg/gY2ksJ3u" target="_blank">Join Newrl Discord<img src="https://user-images.githubusercontent.com/50621007/176236430-53b0f4de-41ff-41f7-92a1-4233890a90c8.png" width="30"/></a>
</p>



<p align="center">
  <img height="150" height="auto" src="https://newrl.net/img/newrl_logo.png">
</p>

# Newrl Mining Testnet
## [Official Guide](https://docs.newrl.net/Validating/running-validator-node/)

## Newrl Miners Setup Guide

### Ports
Run as Root user and Open your VPS port in VPS / Panel
```
sudo su
```
```
sudo ufw allow ssh 
sudo ufw allow 8456
```




### Packages
```
sudo apt update && sudo apt upgrade -y
```

### Depencies
```
sudo apt install -y build-essential libssl-dev libffi-dev git curl screen
```

### Install Python 3.7+
```
sudo apt install python3.9
```

### Install Pip and Python3 venv
```
curl -sSL https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python3 get-pip.py
sudo apt install python3.9-venv
```
```
sudo mkdir newrl-venv
cd newrl-venv
sudo python3.9 -m venv newrl-venv
```

### Activate your environment
```
source newrl-venv/bin/activate
```

### Download and Build Binaries
```
git clone https://github.com/newrlfoundation/newrl.git
cd newrl
scripts/install.sh mainnet
```

### Create wallet
```
python3 scripts/show_wallet.py
```
You will get an output like this 
![image](https://user-images.githubusercontent.com/34649601/193610661-b0667d5c-09d4-4740-82e1-e8c26278b883.png)

Save it somewhere safe!!!

### Importing your wallet

- Go to [Newrl Wallet](https://wallet.newrl.net/) and add phrase then click import
- Copy `{"public": "a9daa99fa288243adb8a3063c0f51261acf75b7a4178c25ede8226xxxxxxxxxxxxxxx", "private": "67095c002fc038xxxxxxxxxxxxxxxxxxxxxxxxxxx", "address": "0x5e7df94d2c134bfd5xxxxxxxxxxxxxxxx"}` to import your wallet then ask for faucet
- Go to [Newrl Faucet](https://wallet.newrl.net/faucet/) and ask for faucet

### Start Node
```
screen -S newrl
scripts/start.sh mainnet
```

To detach from the screen simply press `CTRL+A+D`

To see list of running screen type `screen -r` or `screen -ls`

To restore screen simply run `screen -r <sessionid>`


## Stake your token

- Click on `Run a Node` button on Newrl wallet website and Stake 500k NWRL
![image](https://user-images.githubusercontent.com/34649601/193604862-dff6588b-48e0-4287-8090-d296c5801d42.png)



Then everything is done ! 

Happy Mining!~

