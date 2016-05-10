---
title: Create and Restore HD wallet
visible: false
meta:
    author: Dasource
    updated: 1. 10. 2015
---

## Create and Restore HD wallet

When you first load the new HD wallet it will create a new HD account for you and set it as default, i.e. any new addresses generated will be from the default HD account (unique to you). However as this is pre-generated and not user friendly to remember I suggest you proceed to create a new account using a mnemonic sentence.

**Always backup your wallet.dat first!**

### Creating HD wallet

1. Save your ```wallet.dat``` and rename it
2. Load the latest Shadow wallet
3. Create a new HD wallet (Options > Key Management > New Key) and give it a name
4. Go to "Key Management > Advanced Management" and make sure that the new account (you just named) is showing as "default"
5. The wallet will pre-generate a default normal and stealth addresses
6. Send some funds (few SDC) from your old wallet to the new one

Now let's try to restore this account to test it:

### Recovering HD wallet

1. Save your ```wallet.dat``` and rename it
2. Load the latest Shadow wallet
3. Go to "Options > Key Management > Restore" and complete steps
4. Go to "Help > Debug > Console" and type ```scanforalltxns 590000```
5. You should see your test transaction show up

If all works, you know you have the correct mnemonic and can then go back to your old wallet and send all your funds to the new wallet. Your new HD wallet is setup and the mnemonic sentence + optional pass-code is all you need to access all new addresses.
