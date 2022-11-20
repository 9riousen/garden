---
title: "quartz config"
date: '2022-11-20'
---
- quartz의 `config.toml`은 그냥 [hugo의 것](https://gohugo.io/getting-started/configuration/)이다
- 그럼 quartz의 역할은?
	- github actions
	- template
- Configuration
	- [Configure Dates](https://gohugo.io/getting-started/configuration/)
	- `config.toml`의 `[frontmatter]`부분을 제거하는게 좋을 듯
		- 아니 해결되지 않음. 대신 markdown rendering 부분이 바뀐 듯
	- [`enableEmoji`](https://gohugo.io/getting-started/configuration/#enableemoji) 도 `true`로 변경
		- <https://www.webfx.com/tools/emoji-cheat-sheet/>
---
[[tags/Digital Garden]]