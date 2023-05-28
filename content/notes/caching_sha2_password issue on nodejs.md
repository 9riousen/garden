---
title: "MySQL, NodeJS, caching_sha2_password"
date: '2023-05-28'
images: ['https://i.stack.imgur.com/m0E1M.png']
---
![caching_sha2_password](https://i.stack.imgur.com/m0E1M.png)
- MySQL 8부터는 기본으로 `caching_sha2_password` plugin이 채용됨
- [mysqljs/mysql](https://www.npmjs.com/package/mysql) 에서 이를 지원 못함
```
Failed to connect to MySQL Error: ER_NOT_SUPPORTED_AUTH_MODE: Client does not support authentication protocol requested by server; consider upgrading MySQL client
```
- [해당 user가 다른 plugin을 사용하도록 하거나](https://1mini2.tistory.com/88)
- [mysql2 라는 다른 라이브러리를 사용](https://velog.io/@nohsangwoo/nodejs-mysql-cachingsha2password-plugin)하면 된다
---
- [[tags/NodeJS|NodeJS]]
- [MySQL 8.0 - Nodejs 연동 시 에러 "Client does not support... - i-mini"](https://1mini2.tistory.com/88)
- [nodejs - mysql - caching_sha2_password plugin - nohsangwoo.log](https://velog.io/@nohsangwoo/nodejs-mysql-cachingsha2password-plugin)
- [sidorares/node-mysql2](https://github.com/sidorares/node-mysql2)
