---
title: "RSA vs ECDSA"
date: '2023-01-02'
images: ['https://assets.getwildcard.com/system/images/imgs/000/000/059/original/ecc_rsa.jpg?1458570181']
---
![RSA vs ECDSA](https://assets.getwildcard.com/system/images/imgs/000/000/059/original/ecc_rsa.jpg?1458570181)

| |RSA|ECDSA|
|-|---|-----|
|개발시기|1977년|2005년|
|동작원리|두 소수(prime number)의 곱|타원곡선 방정식|
|Key길이 & 성능|길고 느림|(상대적으로)짧고 빠름|
|Key Pair 생성|한번에 pair생성|임의의 값을 private key로 삼고 public key를 derive|

- [[notes/RSA]]: Rivet, Shamir, Adleman
- ECDSA: Elliptic Curve Digital Signature Algorithm
	- $$(y^2 = x^3 + ax + b)$$
---
- [[tags/Cryptography]]
- [ECDSA vs RSA: Everything You Need to Know](https://sectigostore.com/blog/ecdsa-vs-rsa-everything-you-need-to-know/)
- [EC Signature Generate & Verification](https://8gwifi.org/ecsignverify.jsp)