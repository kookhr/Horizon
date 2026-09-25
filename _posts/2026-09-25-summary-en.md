---
layout: default
title: "Horizon Summary: 2026-09-25 (EN)"
date: 2026-09-25
lang: en
---

> From 33 items, 1 important content pieces were selected

---

1. [Apple Disables Advanced Data Protection in UK Rather Than Build Encryption Backdoor](#item-1) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Apple Disables Advanced Data Protection in UK Rather Than Build Encryption Backdoor](https://macanorak.com/two-tier-encryption-in-the-uk/) ⭐️ 8.0/10

Apple has disabled Advanced Data Protection (ADP) for iCloud users in the United Kingdom after the UK government issued a legal order demanding access to encrypted user data. Rather than compromise its encryption architecture by building a backdoor, Apple chose to stop offering ADP entirely in the UK, reverting affected data categories to Standard Data Protection where Apple holds the encryption keys. This decision creates a two-tier encryption landscape where UK users have weaker data protection than users in other countries, setting a precedent that could embolden other governments to make similar demands. It also represents a significant shift in the global encryption debate, demonstrating that governments can effectively pressure companies into reducing security even without explicitly banning end-to-end encryption. ADP expands end-to-end encryption from 14 default iCloud categories (including iCloud Keychain and Health data) to 23 total categories, adding protection for iCloud Backup, Photos, Notes, and iCloud Drive. With ADP disabled, UK users' data in those 9 additional categories reverts to Standard Data Protection, where Apple holds the keys and can comply with lawful access requests; however, the 14 baseline E2EE categories remain protected.

hackernews · ReturnoftheHack · Sep 24, 10:39 · [Discussion](https://news.ycombinator.com/item?id=49828731)

**Background**: Advanced Data Protection (ADP) is an optional iCloud setting introduced by Apple in December 2022 that provides the company's highest level of cloud data security by applying end-to-end encryption to additional data categories beyond the 14 that are E2EE by default. Under Standard Data Protection, Apple holds the encryption keys and can decrypt user data in response to lawful government requests, while E2EE ensures only the user's trusted devices can decrypt the data. The UK government has been pursuing expanded surveillance powers under the Investigatory Powers Act, which can compel companies to provide access to user data and, critically, prohibits companies from publicly disclosing such demands. An encryption backdoor is a deliberate method of bypassing normal encryption, which security experts broadly argue creates vulnerabilities that can be exploited by malicious actors, not just governments.

<details><summary>References</summary>
<ul>
<li><a href="https://support.apple.com/en-us/108756">How to turn on Advanced Data Protection for iCloud</a></li>
<li><a href="https://en.wikipedia.org/wiki/Encryption_backdoor">Encryption backdoor</a></li>
<li><a href="https://www.internetsociety.org/blog/2025/05/what-is-an-encryption-backdoor/">What Is an Encryption Backdoor? - Internet Society</a></li>

</ul>
</details>

**Discussion**: Community sentiment is largely critical of Apple, with many commenters contrasting the company's current capitulation with its 2015 stance against the FBI, arguing that Apple has lost its willingness to fight for user privacy. Technical discussions highlight that even the 14 baseline E2EE categories are effectively compromised because secrets stored in iCloud Keychain can be exposed through unencrypted iCloud Backup. Several users expressed frustration that the UK government can secretly demand backdoors without allowing public disclosure, effectively outlawing E2EE by stealth, while others called for Apple to withdraw entirely from the UK market.

**Tags**: `#encryption`, `#privacy`, `#apple`, `#uk-policy`, `#surveillance`

---