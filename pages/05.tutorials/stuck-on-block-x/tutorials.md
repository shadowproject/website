---
title: I'm stuck on block X, what do I do?
visible: false
meta:
    author: Code
    updated: 30. 6. 2016
---

## I'm stuck on block X, what do I do?

If your client won't sync anymore, it hasn't loaded any blocks the past few hours or even days. Here is what you do:

* Close your ShadowCash wallet.
* Open up the ```shadowcoin.conf``` file in the ShadowCoin directory.

| OS | Path to directory |
| ------ | ------ |
| Windows | ```%appdata%\ShadowCoin``` |
| Linux | ```~/.shadowcoin``` |
| OSX | ```~/Library/Application Support/ShadowCoin``` |

* Open up your ```shadowcoin.conf``` file and add the following:

```
addnode=explorer.shadow.cash
```

This will connect your node to the shadow.cash explorer; **this does however reduce anonymity**.

* Open up your ShadowCash client and go to ```Help > Debug Window > Command Interface``` and type in:

```
rewindchain 1000
```

This will remove the last 1000 blocks and redownload them.

* Let the blockchain catch up, and it should be fixed.

<div class="message">If it's not fixed then I advice you to try the blockchain method: <a href="fast-sync-blockchain">Faster Sync with Blockchain.zip</a></div>