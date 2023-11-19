---
title: .nvmrc (프로젝트별 node version)
date: 2023-11-19
images:
  - https://miro.medium.com/v2/resize:fit:737/1*gsFp-xRynToQB54shinULA.png
---
![.nvmrc](https://miro.medium.com/v2/resize:fit:737/1*gsFp-xRynToQB54shinULA.png)
- 현재 repo가 사용할 node version을 명시 (해당 디렉토리에서 `nvm use`를 사용하여 해당 버젼의 nodejs 사용)

```bash
$ echo "18" > .nvmrc   # 다른 버젼은 `nvm ls-remote`
$ nvm use
```

---
- [[tags/NodeJS|NodeJS]]
- [[notes/nvm|nvm]]
- [.nvmrc | nvm-sh GitHub](https://github.com/nvm-sh/nvm#nvmrc)
