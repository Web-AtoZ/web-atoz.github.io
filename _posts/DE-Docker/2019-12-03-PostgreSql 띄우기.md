---
layout: post
title:  PostgreSql 띄우기
comments: true
categories : [Development Environment/Docker]
tags: [Docker, PostgreSql]
author: hanseonghye
---



## 실행 명령어 

```shell
> docker run -p 5432:5432 -e POSTGRES_PASSWORD=비밀번호 -e POSTGRES_USER=사용자이름 -e POSTGRES_DB=디비명 --name 컨테이너이름 -d postgres
```



<br/><br/>

## 로컬에서 확인하기

<br/>

### 커널에서 확인하기

1. 도커 서버에 접속하기 ?

```shell
> docker exec -i -t 컨테이너이름 bash
```

2. psql 접속

```
> su - postgres
> psql --username 사용자이름 --dbname db이름
```

<br/>

### 데이터 베이스 툴로 확인하기

postgresql 데이터 베이스 툴을 통해 연결이 됐는지 확인해 보자.

인코딩 에러가 발생한다. compose.yml??여기서 셋팅하라는데 모르겠다.