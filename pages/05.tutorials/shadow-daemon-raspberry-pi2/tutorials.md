---
title: Compile Shadow Daemon on Raspberry Pi 2 (Raspbian Jessie) and beyond
visible: false
meta:
    author: Litebit
    updated: 11. 5. 2016
---

## Compile Shadow Daemon on Raspberry Pi 2 (Raspbian Jessie) and beyond

### Requirements

* Full disk image of [Raspbian Jessie](https://www.raspberrypi.org/downloads/raspbian/)
* Instructions on [installing Raspberry Pi operating software](https://www.raspberrypi.org/documentation/installation/installing-images/README.md)
* [Change Swapfile size](https://raspberrypi.stackexchange.com/questions/70/how-to-set-up-swap-space) on Raspberry Pi (2GB should work)


### Getting Started

<div class="message">Beginner Hint – only copy code after "$"</div>

Update and install dependencies:

```
$ sudo apt-get update && sudo apt-get upgrade
$ sudo apt-get install git build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev libqrencode-dev
```

Download Shadow source code:

```
$ git clone https://github.com/ShadowProject/shadow
$ cd shadow/src
```

Download and build upnpc:

```
~/shadow/src $ wget http://miniupnp.tuxfamily.org/files/miniupnpc-1.9.20160209.tar.gz
~/shadow/src $ tar -xzvf miniupnpc-1.9.20160209.tar.gz
~/shadow/src $ cd miniupnpc-1.9.20160209
~/shadow/src/miniupnpc-1.9.20160209 $ make
~/shadow/src/miniupnpc-1.9.20160209 $ sudo su
~/shadow/src/miniupnpc-1.9.20160209 $ make install
```

* ```exit``` to exit root access
* ```cd ..``` returns you to /shadow/src

Compile Shadow source code (shadowcoind):

```
~/shadow/src $ make -f makefile.unix -j 3
~/shadow/src $ strip shadowcoind
```

Run Shadow daemon (shadowcoind):

```
~/shadow/src $ ./shadowcoind
```

* On the inital start-up **shadowcoind** will return an error because it cannot find the configuration file **shadowcoin.conf**

Create Shadow configuration file (shadowcoin.conf):

```
~/shadow/src $ nano ~/.shadowcoin/shadowcoin.conf
```

* Add the following to your configuration file, changing the **username** and **password** to something secure:

```
daemon=1
rpcuser=[secure username]
rpcpassword=[secure password]
addnode=blockexplorerip
```

1. Exit: **[Ctrl] + [X]**
2. Save: **[Y]**
3. **[Enter]**

Run Shadow daemon (shadowcoind):

```
~/shadow/src $ ./shadowcoind
```


### Stay Updated

Update Shadow source code:

```
~/shadow/src $ git pull
```

Compile Shadow source code:

```
~/shadow/src $ make -f makefile.unix -j 3
~/shadow/src $ strip shadowcoin
```

Run Shadow daemon (shadowcoind):

```
~/shadow/src $ ./shadowcoind
```


### Troubleshooting

| Problem | Solution |
|---------|----------|
| Virtual memory exhausted: Cannot allocate memory | [Increase swapfile size](https://raspberrypi.stackexchange.com/questions/70/how-to-set-up-swap-space) - (2GB should work) |
| g++: internal compiler error: Killed (program cc1plus) | [Increase swapfile size](https://raspberrypi.stackexchange.com/questions/70/how-to-set-up-swap-space) - (2GB should work) |
| Corrupt /obj/extkey.o caused by interrupted previous build | Delete it before trying to re-compile |


### Resources

* [JSON-RPS API commands](https://doc.shadowproject.io/#json-rpc-api-reference)
