---
title: "KDF: Key Derivation Function"
date: 2023-09-02
images:
  - https://www.baeldung.com/wp-content/uploads/sites/4/2023/06/KDF.png
---
![KDF](https://www.baeldung.com/wp-content/uploads/sites/4/2023/06/KDF.png)
- [password hashing function](https://en.wikipedia.org/w/index.php?title=Password-hashing_function)과 동의어
- binary형식의 key 보단 text 형식의 password가 필요할 때 사용하는 hash function
- PBKDF2, bcrypt, scrypt 등이 KDF에 속함
	- bcrypt의 `b`는 사용한 크립토 라이브러리인 blowfish에서 왔다
---
- [[tags/Cryptography|Cryptography]]
- [KDF: Deriving Key from Password - Practical Cryptography for Developers](https://cryptobook.nakov.com/mac-and-key-derivation/kdf-deriving-key-from-password)
- [Password hashing in Node.js with bcrypt](https://blog.logrocket.com/password-hashing-node-js-bcrypt/)
