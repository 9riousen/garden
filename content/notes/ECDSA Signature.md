---
title: "ECDSA Signature (r,v)"
date: '2023-01-03'
images: ['https://miro.medium.com/max/1160/1*fN1sBKNvVScvbpEFwyZR0Q.png']
---
![ECDSA Signature](https://miro.medium.com/max/1160/1*fN1sBKNvVScvbpEFwyZR0Q.png)

- [[tags/TODO]] 아직 이해 안되는 부분이 많다
- PKI의 signature라는게 privake key로 hash하는게 전부겠지 라고 생각했는데 영 모르겠다
- signature가 그냥 문자열로 나올것으로 기대했는데 `(r,s)` pair로 나옴
- [어떤 곳](https://8gwifi.org/ecsignverify.jsp)에선 signature가 그냥 문자열인데 DER 형식으로 export한거라고 본거 같은데 실험 필요
- [Non-deterministic signature](https://blog.naver.com/PostView.naver?blogId=aepkoreanet&logNo=222621861479) 라는데 정말인지 실험을 못 해봤다 (매번 다르게 나온다는데 실험해 보고 싶다)
- Signature를 검증하려면 상대의 public key가 있어야 하는데 blockchain 세상에서 address만 알지 public key는 모른다 (public key -> address는 가능하지만)
	- ECDSA는 신기하게도 서명과 원본 메세지가 있으면 public key복원이 가능하다 ([Public Key Recovery from Signature](https://cryptobook.nakov.com/digital-signatures/ecdsa-sign-verify-messages#ecdsa-public-key-recovery-from-signature))
	- [ethers.js](https://docs.ethers.org/v5/api/utils/signing-key/#utils-recoverPublicKey)에 원하는 기능이 있지만 javascript ecdsa library 수준에서 테스트 해보려고 하니 의외로 잘 안된다.
	- [작동하는 예제](https://replit.com/@rious9/ECDSA-sign-verify-in-JS#index.js) 작성 성공
		- [이 예제에선 hex2dec()에서 private key가 등장하여 헷깔린다. 사실은 등장할 필요가 없다. BigNumber를 직접 사용하기 귀찮아서 예제를 그렇게 만든 듯](https://gist.github.com/nakov/1dcbe26988e18f7a4d013b65d8803ffc#file-secp256k1-example-js-L25)
---
- [[notes/ECDSA]]
- [EC Signature Generate & Verification](https://8gwifi.org/ecsignverify.jsp)
- [ECDSA 사용시 Signature 값이 매번 다른 이유](https://blog.naver.com/PostView.naver?blogId=aepkoreanet&logNo=222621861479)