---
title: "secp256k1"
date: '2023-01-02'
images: ['https://en.bitcoin.it/w/images/en/b/bf/Secp256k1.png']
---
![secp256k1](https://en.bitcoin.it/w/images/en/b/bf/Secp256k1.png)

**S**tandard for **E**fficient **C**ryptography
- p: Parameter `p` over `Fp`
- 256: Field Size- `p` 의 bit수
- k: Koblitz curve 변경
- 1: sequence number

[[notes/ECDSA]]의 타원곡선인자(ecparam) 중 하나( a=0, b=7 ). 즉,
$$y^2 = x^3 + 7$$
- 위 공식을 [Desmos](https://www.desmos.com/calculator) 같은곳에 입력해 보면 같은 그래프가 그려짐
- Bitcoin에서 먼저 채용되었으며 Ethereum을 포함한 많은 블록체인에서 채용됨
- AEP코리아네트의 블로그에 언급하였듯이 타원곡선 암호기술의 그래프는 타원을 그리지 않는다
> 아래 그림에서 보여 지듯이, “타원곡선” 과  “타원”은 전혀 상관이 없습니다. 그럼에도 불구하고 "타원"이란 단어가 붙어있는 이유는, 수학 역사적으로, 타원의 둘레를 구하기 위해, 적분하는 과정에서 도출된 식이기 때문이라고 합니다.

---
- [[tags/Cryptography]]
- [ECDSA vs RSA: Everything You Need to Know](https://sectigostore.com/blog/ecdsa-vs-rsa-everything-you-need-to-know/)
- [EC Signature Generate & Verification](https://8gwifi.org/ecsignverify.jsp)
- [비트코인에서 사용하는 타원곡선암호기술(ECC) - AEP코리아네트](https://blog.naver.com/aepkoreanet/221178375642)