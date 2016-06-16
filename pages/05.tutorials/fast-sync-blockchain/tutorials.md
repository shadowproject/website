---
title: Faster sync with blockchain.zip
visible: false
meta:
    author: Code
    updated: 9. 5. 2016
---

## Faster sync with blockchain.zip

1. Close Wallet
2. Download [blockchain.zip](https://github.com/ShadowProject/blockchain/releases/download/latest/blockchain.zip) from Shadow GitHub (don't trust any links outside ShadowProject on GitHub!)
3. Delete ```blk001.dat```, ```txleveldb``` from Shadowcoin app directory

| OS | Path to directory |
| ------ | ------ |
| Windows | ```%appdata%\ShadowCoin``` |
| Linux | ```~/.shadowcoin``` |
| OSX | ```~/Library/Application Support/ShadowCoin``` |

4. Extract downloaded file into Shadowcoin app directory
5. Launch Wallet again (let it run even if it becomes unresponsive)
6. When Wallet starts, you should be synced completely (you can check against Block Explorer)