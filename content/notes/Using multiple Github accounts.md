---
title: "여러 github.com 계정 관리하기"
date: '2023-03-12'
images: ['https://tecadmin.net/wp-content/uploads/2020/09/setup-multiple-git-account-on-a-system.png']
---
![multiple git accounts](https://tecadmin.net/wp-content/uploads/2020/09/setup-multiple-git-account-on-a-system.png)

- [이 글](https://velog.io/@grr1203/%ED%95%9C-%EC%BB%B4%ED%93%A8%ED%84%B0%EC%97%90%EC%84%9C-Github-%EA%B3%84%EC%A0%95-%EC%97%AC%EB%9F%AC%EA%B0%9C-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0)이 한글이라 좋다
- 가끔 세팅하기 때문에 매번 까먹는다
- 그런데 ssh-agent의 용도는 이해 못했다. (`ssh-add` 안하면 동작 안하는가?)
- 3번의 `~/.ssh/config` 에 ssh keypair를 여러개 생성하고 설정하는 부분 중요
- 4-1에서 clone할 때 `git@github.com` 대신 `~/.ssh/config` 에서 내가 설정한 hostname을 지정하는게 중요
- 4-2에서 local의 project directory에서 `git config user.email user1@example.com` 설정하는 게 중요
	- 이 설정은 `{PROJECT_ROOT}/.git/config`에 저장된다

---
- [[tags/git]]
- [한 컴퓨터에서 Github 계정 여러개 사용하기 - dolanap.log](https://velog.io/@grr1203/%ED%95%9C-%EC%BB%B4%ED%93%A8%ED%84%B0%EC%97%90%EC%84%9C-Github-%EA%B3%84%EC%A0%95-%EC%97%AC%EB%9F%AC%EA%B0%9C-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0)