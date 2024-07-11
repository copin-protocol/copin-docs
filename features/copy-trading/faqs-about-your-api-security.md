---
description: >-
  Frequently asked questions and things to know about your API from
  CEXs(@binane, @bybit,...) security on Copin!
---

# FAQs about your API security

### 1. Can Copin withdraw your assets via API?

* No, we only require API access to your "derivatives" wallet. We are not permitted to access any of your other wallets, including but not limited to: Spot, P2P, Funding, etc.
* Even CEX platforms do not allow withdrawing users' assets via API.

### 2. How does Copin store your API keys?

* We store them following the [OWASP](https://www.cloudflare.com/learning/security/threats/owasp-top-10/) security standards (similar to how user passwords are stored).
* All critical information about users' API keys, such as secret keys or passphrases, is encrypted when stored in our database.
* Therefore, even if our database is hacked, the hacker will not be able to access your API keys.

### 3. **How can I make my API keys more secure?**

* Never share your API key and secret with anyone.
* We recommend creating new and updating your API keys every 30 days.
