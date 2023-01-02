---
title: "ECDSA (Elliptic Curve Digital Signature Algorithm)"
date: '2023-01-02'
images: ['https://academy.bit2me.com/wp-content/uploads/2019/04/42_ECDSA.png']
---
![ECDSA](https://academy.bit2me.com/wp-content/uploads/2019/04/42_ECDSA.png)

타원곡선암호(ECC; Elliptic Curve Cryptosystem)에 기반을 둔 전자서명 알고리즘
$$(y^2 = x^3 + ax + b)$$
위의 형태를 가짐. `a`와 `b` 값 조합을 ecparam (Elliptic Curve Parameters)라고 하며 대표적으로 [[notes/secp256k1]] 이 있다.

---
- [[tags/Cryptography]]
- [ECDSA vs RSA: Everything You Need to Know](https://sectigostore.com/blog/ecdsa-vs-rsa-everything-you-need-to-know/)
- [EC Signature Generate & Verification](https://8gwifi.org/ecsignverify.jsp)
- [타원곡선 디지털서명 알고리즘 - 해시넷](http://wiki.hash.kr/index.php/%ED%83%80%EC%9B%90%EA%B3%A1%EC%84%A0_%EB%94%94%EC%A7%80%ED%84%B8%EC%84%9C%EB%AA%85_%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98)