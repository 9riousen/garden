---
title: "Regression (회귀분석)"
date: '2023-07-09'
images: ['https://miro.medium.com/v2/resize:fit:1200/1*N1-K-A43_98pYZ27fnupDA.jpeg']
---
![Regression](https://miro.medium.com/v2/resize:fit:1200/1*N1-K-A43_98pYZ27fnupDA.jpeg)

# 개인적 견해
- 대세 흐름을 기준으로 얼마나 실데이터가 차이나는지를 다루는 방법
- 영어도 한국말도 감이 잘 안오긴 한다.
- '회귀'는 '결국 돌아온다'의 느낌인데 "가끔 이상한 데이터가 있어도 크게보면 이렇게 돌아온다" 정도
- 결국 엑셀에서 차트그려보고 interpolation 하는 방법정도

# 독립변수 vs 종속변수
- `y = f(x)` : `x`는 독립변수(independent variable). 이에 따라 `y`가 결정되니까 `y`는 종속변수(dependent variable)
- `z = f(x,y)` : `x`와 `y`는 독립변수, `z`는 종속변수
- 회귀분석은 어떤 특성(독립변수)을 조사하여 어떤 영향(종속변수)이 생기는지의 통찰을 얻는 과정. 통찰이 생기면 예측이 가능해 진다
- "회귀 모형(regression model)을 만든다"의 의미
	- `f()` 의 body를 구현한다
	- `y = b + m * x` 에서 `m`과 `b`를 찾는다
	- 차트의 선을 그리는 공식을 찾는다

# 역사
- 생물학에서 '평균으로의 회귀(regression to the mean)' 현상을 증명하려고 만들어졌다 ([나무위키](https://namu.wiki/w/%ED%9A%8C%EA%B7%80%20%EB%B6%84%EC%84%9D#s-2))

---
- [[tags/AI|AI]]
- [회귀분석 | 나무위키](https://namu.wiki/w/%ED%9A%8C%EA%B7%80%20%EB%B6%84%EC%84%9D)