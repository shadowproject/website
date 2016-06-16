---
title: How to validate SHA256 checksums of official Shadow releases
visible: false
meta:
    author: Litebit
    updated: 10. 5. 2016
---

## How to validate SHA256 checksums of official Shadow releases

### What is a checksum and who cares?

While compiling from source is the recommended and most secure way to build the Shadow platform, the team realizes this is an advanced technique that a large number of users aren't comfortable with. For most users, each release is distributed with source code and pre-compiled distributions for Windows, Mac & Linux.

To ensure the highest level of security, the Shadow Project team provides sha256sums for all of these releases. Each checksum is a hash of the download file that verify nothing has been added or taken away either in-transit or by a third party. By using sha256 encryption with these sums every computer will generate the same hash unless the file has been compromised, which in response, will generate a different hash.

**It is recommended to always validate the Shadow build releases with the provided sha256sums.**


### Validate Shadow checksums on Linux

Most Linux distributions come with the **sha256sum**.

<div class="message">Beginner Hint – only copy code after "$"</div>

1. Download latest Linux release from Github:

```
$ cd Downloads
~/Downloads$ wget https://github.com/shadowproject/shadow/releases/download/v1.4.0.3/shadow_1.4.0.3_linux64.zip
```

2. Run sha256sum on downloaded file:

```
~/Downloads$ sha256sum shadow_1.4.0.3_linux64.zip
```

**sha256sum** hash result: ```baf8b6ebeac7e7bf2f21ed53f34735a8d3db98e91a7245212533532ec4acb567```

3. compare sha256sum of downloaded file to official file:

* Visit https://github.com/shadowproject/shadow/releases/tag/v1.4.0.3
* Find "**sha256sums**" section
* Verify sha256sum for "**shadow_1.4.0.3_linux64.zip**" file:

```
baf8b6ebeac7e7bf2f21ed53f34735a8d3db98e91a7245212533532ec4acb567 shadow_1.4.0.3_linux64.zip
```

**Ensure both checksums are identical before installing software!**


### Validate Shadow checksums on the web

There are a number of hash generators online, this tutorial will highlight [Hash Online Convert](http://hash.online-convert.com/sha256-generator)

1. Download preferred Shadow OS release from GitHub [e.g. Windows client](https://github.com/shadowproject/shadow/releases/download/v1.4.0.3/shadow_1.4.0.3_win64.zip)
2. Visit [Hash Online Convert](http://hash.online-convert.com/sha256-generator)

* Find "**Or upload and generate a SHA-256 checksum of a file:**" section
* Select "**Choose File**" button
* Find downloaded Shadow OS release file
* Select "**Open**" button
* Select "**Convert file**" button

3. Hash converter: File gets submitted to the website and loads a new page showing _"Your hash has been successfully generated."_ This page shows the hash of the uploaded file in a variety of hash outputs; hex, HEX, h:e:x & base64 – Value to look for: **hex** ``` 68844337c068dcb773c58991d5b29b8f5701de43d6bd64fe1c55c468c61fe737```
4. Compare sha256sum of downloaded file to official file:

* Visit https://github.com/shadowproject/shadow/releases/tag/v1.4.0.3
* Find "**sha256sums**" section
* Verify sha256sum for "**shadow_1.4.0.3_win64.zip**" file:

```
68844337c068dcb773c58991d5b29b8f5701de43d6bd64fe1c55c468c61fe737 shadow_1.4.0.3_win64.zip
```

**Ensure both checksums are identical before installing software!**
