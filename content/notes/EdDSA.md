---
title: "EdDSA"
date: '2021-12-04'
---
![EdDSA+Ed25519](https://pbs.twimg.com/media/ELBiumwVUAAiNId.jpg)
- ECDSA 보다 신형 (2012)
- 더 빠르면서도 안전하다
- DSA, ECDSA는 insecure하다고 치부하기도 함
- 신형이라 아직 지원하지 않는 library나 tool이 많다
- OpenSSH 6.5 (2014) 이상에서 제공
	- [How to generate secure SSH keys](https://www.adsmurai.com/en/articles/how-to-generate-secure-ssh-keys)
```jsx
ssh-keygen -t ed25519
```

---
[[tags/Glossary]] [[tags/Blockchain]]