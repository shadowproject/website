---
title: 'Bug Bounties'
---

## SHADOW BUG & BOUNTY PROGRAM

According to [Linus’ Law](http://en.wikipedia.org/wiki/Linus), _“given enough eyeballs, all bugs are shallow”_. That’s one of the reasons why Shadow’s source code is publicly available; but merely making the source code available doesn’t accomplish anything if people don’t read it!

For this reason, Shadow has a series of bug bounties. Similar to the bounties offered by [Mozilla](http://www.mozilla.org/security/bug-bounty.html) and [Google](http://blog.chromium.org/2010/01/encouraging-more-chromium-security.html), Shadow bug bounties provide an opportunity for people who find bugs to be compensated. Unlike those programs, however, Shadow’s bounties are not limited to security vulnerabilities.

Depending on the type of bug and when it is reported, different bounties will be awarded. Bounties are paid out in SDC, at the 3-day average of each to a fixed US Dollar value.

### Things that do not qualify under the bug bounty

- Bugs found on third-party/community sites, software or services, which is not due to an improper configuration issue specific to us. Please submit any potential issues to the maintainers of that site or providers of that service.
- Vulnerabilities which are too broad or not documented properly (i.e. do not include a specific example relevant to a Shadow-controlled site or application).
- Bugs or issues with a third-party site, software, or service that we use, which is not due to an improper configuration issue specific to us. Please submit any potential issues to the maintainers of that site or providers of that service.
- Bugs and errors found in software/code that is still undergoing alpha or beta testing.
- Usability issues
- Anything requiring social engineering
- DOS/DDOS attacks
- Missing HSTS (HttpOnly flags), Secure flag, Browser Cache vulnerabilities
- CSRF that doesn’t affect the victim
- Referrer leakage to pages an attacker cannot control.
- The presence of unnecessary files, e.g. for backups, when these files do not expose any sensitive information.
- Anything that is the result of an automated Nessus/PCI scans (too general)
- DNS issues (e.g. lack of an SPF record)
- SSL certificate issues
- Bugs that have received mainstream tech media or community attention before the date of your disclosure.

## BUG BOUNTIES & REWARDS

Depending on the type of bug and when it is reported, different bounties will be awarded. Bounties are paid out in SDC, at the 3-day average of each to a fixed US Dollar value.

**Please do not report security vulnerabilities publicly.**

Reward | Bug
--- | ---
**$1500** | Deanonymize ShadowChat or ShadowSend (proof that a protocol is not anonymous)
**$750** | A flaw in the protocol that allows for theft or loss of funds
**$500** | A bug in the reference client that leads to consensus issues
**$250** | A bug which causes data corruption or loss
**$100** | A bug which causes the application to crash
**$50** | Other non-harmless bugs
**$10** | 'Harmless' bugs, e.g. cosmetic errors

<div class="message"><em>Note</em> — Bounties will be paid out for bugs found in the <a href="https://github.com/ShadowProject/shadow/tree/master">master branch of the official GitHub repositories</a> (en)</div>