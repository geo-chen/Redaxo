# CVE-2024–13209 - Redaxo CMS 5.18.1 Cross Site Scripting

## Vulnerability

Stored XSS on REDAXO 5.18.1 — Article / “content/edit”

On the latest version of Redaxo, v5.18.1, the article name field is susceptible to stored XSS.

If a user creates an article name (ie /redaxo/index.php?page=structure&category_id=1&article_id=1&clang=1&function=edit_art&artstart=0) using a xss payload such as “<BODY ONLOAD=alert(‘XSS!’)>”, the XSS executes.

A malicious actor can easily steal cookie using this stored XSS and perform a session hijacking attack.
![image](https://github.com/user-attachments/assets/a4e568d4-f2b2-4d14-bc1d-a6050710f9c1)

![image](https://github.com/user-attachments/assets/9495d2da-f5e1-4e08-ab2a-cf6817997b52)

## Impact
A malicious actor can easily steal cookie using this stored XSS and perform a session hijacking attack.

![image](https://github.com/user-attachments/assets/439011ad-7fe4-465b-b221-f52bccaf493c)

## Disclosure
Informed the Redaxo team via email and github.

## Reference
https://github.com/redaxo/redaxo/security/advisories/GHSA-7wj8-856p-qc9m
https://vuldb.com/?id.290814
