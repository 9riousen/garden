---
title: "Compressed Public Key"
date: '2023-03-04'
images: ['https://products.mpowerpromo.com/AMERICANNA/CS-5KY/CS-5KY-BF/big/CS-5KY-BF.png']
---
![Compressed Public Key](https://products.mpowerpromo.com/AMERICANNA/CS-5KY/CS-5KY-BF/big/CS-5KY-BF.png)
- [[notes/secp256k1]] curve는 Bitcoin과 Ethereum의 키생성 알고리즘으로 채택되며 사실상 표준이다
- 수학적 설명은 모르겠고 public key는 압축이 가능하다 (zip같은 압축이 아니다)
	- uncompressed public key: 65 bytes
	- compressed public key: 33 bytes
- 위 둘은 서로 손실없이 전환 가능하다 (따라서 compressed public key가 많이 사용됨)
- 익숙한 64byte, 32byte가 아닌 이유는 제일 앞에 1바이트를 추가하기 때문이다
	- `02`나 `03`으로 시작하면 compressed public key라는 뜻이다.
		- `0252972572d465d016d4c501887b8df303eee3ed602c056b1eb09260dfa0da0ab2`
		- `0318ed2e1ec629e2d3dae7be1103d4f911c24e0c80e70038f5eb5548245c475f50`
	- `04`로 시작하면 uncompressed public key라는 뜻이다
		- `52972572d465d016d4c501887b8df303eee3ed602c056b1eb09260dfa0da0ab288742f4dc97d9edb6fd946babc002fdfb06f26caf117b9405ed79275763fdb1c`
- [[notes/secp256k1]] 에서 어떤 x좌표의 y값이 2개가 나온다
	- 따라서 x,y를 각각 32byte씩 64byte로 표현하는 것이 uncompressed public key
	- x만 32 byte기재하고 y는 둘중 어떤것인지 첫바이트로 기재하는 것이 compressed public key
	- 즉, 육안으로 봐도 compressed-uncompressed 가 맞게 변환 되었는지 어느정도 확인이 된다
		- x좌표는 같이 때문에 compressed의 첫 1바이트(2 hex digit)을 제외한 나머지가 uncompressed 에도 똑같이 나타남

---
- [[tags/Cryptography]]
- [[tags/Blockchain]]
- [02,03 or 04? So what are compressed and uncompressed public keys](https://medium.com/asecuritysite-when-bob-met-alice/02-03-or-04-so-what-are-compressed-and-uncompressed-public-keys-6abcb57efeb6)