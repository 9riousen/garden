---
title: "secp256k1"
date: '2023-01-02'
images: ['https://en.bitcoin.it/w/images/en/b/bf/Secp256k1.png']
---
![secp256k1](https://en.bitcoin.it/w/images/en/b/bf/Secp256k1.png)

[[notes/ECDSA]]의 타원곡선인자(ecparam) 중 하나( a=0, b=7 ). 즉,
$$y^2 = x^3 + 7$$
- 위 공식을 [Desmos](https://www.desmos.com/calculator) 같은곳에 입력해 보면 같은 그래프가 그려짐
- Bitcoin에서 먼저 채용되었으며 Ethereum을 포함한 많은 블록체인에서 채용됨

---
- [[tags/Cryptography]]
- [ECDSA vs RSA: Everything You Need to Know](https://sectigostore.com/blog/ecdsa-vs-rsa-everything-you-need-to-know/)
- [EC Signature Generate & Verification](https://8gwifi.org/ecsignverify.jsp)
- [비트코인에서 사용하는 타원곡선암호기술(ECC)](https://blog.naver.com/aepkoreanet/221178375642)