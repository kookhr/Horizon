---
layout: default
title: "Horizon Summary: 2026-09-25 (ZH)"
date: 2026-09-25
lang: zh
---

> 从 33 条内容中筛选出 1 条重要资讯。

---

1. [苹果在英国停用高级数据保护而非构建加密后门](#item-1) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [苹果在英国停用高级数据保护而非构建加密后门](https://macanorak.com/two-tier-encryption-in-the-uk/) ⭐️ 8.0/10

在英国政府发出要求访问加密用户数据的法律命令后，苹果已为英国 iCloud 用户停用了高级数据保护（ADP）。苹果没有通过构建后门来妥协其加密架构，而是选择在英国完全停止提供 ADP，将受影响的数据类别恢复为苹果持有加密密钥的标准数据保护。 这一决定创造了一个双层加密格局，英国用户的数据保护弱于其他国家的用户，这可能开创先例，鼓励其他政府提出类似要求。它也代表了全球加密辩论的重大转变，表明政府可以在不明确禁止端到端加密的情况下，有效迫使企业降低安全标准。 ADP 将端到端加密从 14 个默认 iCloud 类别（包括 iCloud 钥匙串和健康数据）扩展到 23 个类别，为 iCloud 备份、照片、备忘录和 iCloud 云盘增加保护。ADP 被停用后，英国用户在这 9 个额外类别中的数据恢复为标准数据保护，苹果持有密钥并可配合合法访问请求；但 14 个基础端到端加密类别仍受保护。

hackernews · ReturnoftheHack · 9月24日 10:39 · [社区讨论](https://news.ycombinator.com/item?id=49828731)

**背景**: 高级数据保护（ADP）是苹果于 2022 年 12 月推出的可选 iCloud 设置，通过在 14 个默认端到端加密类别之外对更多数据类别应用端到端加密，提供该公司最高级别的云数据安全。在标准数据保护下，苹果持有加密密钥，可以响应合法的政府请求解密用户数据，而端到端加密确保只有用户受信任的设备才能解密数据。英国政府一直在依据《调查权力法》扩大监控权力，该法可强制企业提供用户数据访问权限，且关键的是，禁止企业公开披露此类要求。加密后门是一种绕过正常加密的蓄意方法，安全专家普遍认为这会创造可被恶意行为者利用的漏洞，而不仅仅是政府。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.apple.com/en-us/108756">How to turn on Advanced Data Protection for iCloud</a></li>
<li><a href="https://en.wikipedia.org/wiki/Encryption_backdoor">Encryption backdoor</a></li>
<li><a href="https://www.internetsociety.org/blog/2025/05/what-is-an-encryption-backdoor/">What Is an Encryption Backdoor? - Internet Society</a></li>

</ul>
</details>

**社区讨论**: 社区情绪主要对苹果持批评态度，许多评论者将公司当前的妥协与 2015 年对抗 FBI 的立场进行对比，认为苹果已失去为用户隐私而战的意愿。技术讨论强调，即使是 14 个基础端到端加密类别也实际上被削弱了，因为存储在 iCloud 钥匙串中的密钥可以通过未加密的 iCloud 备份暴露。一些用户对英国政府可以秘密要求后门而不允许公开披露感到沮丧，认为这实质上是在暗中取缔端到端加密，另一些人则呼吁苹果完全退出英国市场。

**标签**: `#encryption`, `#privacy`, `#apple`, `#uk-policy`, `#surveillance`

---