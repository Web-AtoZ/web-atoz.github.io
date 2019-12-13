---
layout: post
title: 1. 깃허브(Github) 블로그에 카테고리 추가하기
comments: true
categories: [Development Environment/Github Blog]
tags: [Github Blog]
author: jungeunlee95
userImage: /assets/user-img/jungeun.png
---

---

<br>

> <subtitle> [1] html 파일 수정 </subtitle>

카테고리 추가/수정을 원할 시 html파일에서 `div > ul > li 태그`에 카테고리를 추가/수정 해야합니다.

**1. _includes/header.html**

**2. _site/404.html**

**3.  _site/about/index.html** 

📍 <b style="color:red"> 위의 세 파일 모두 공통으로 수정 해야합니다.</b> 📍

<br>

**ex) Project/ Daily 카테고리 추가 시**

```html
<div class="site-category">
    <ul class='cat1'>
        <li><a href="/">Home</a></li>
        
        ... 생략 ...
        
        <li><a href="/">Project</a>
            <ul>
                <li><a href="/Project/Daily">Daily</a></li>
            </ul>
        </li>
		
        ... 생략 ...

    </ul>
</div>
```

------

<br>

> <subtitle> [2] category/ 위치에 설정 파일 추가 </subtitle>

**category/{{카테고리이름}}.md** 파일 추가

ex) Project/Daily 카테고리 추가 시 **category/Daily.md** 파일 생성 후 하기의 내용 작성

```
---
layout: category
title: Project/Daily
permalink: 'Project/Daily'
---

Another sample category page.
```

---

<br>

> <subtitle> [3] Post 작성 시 .md 파일 상단에 카테고리 설정 후 작성 </subtitle>

ex) 2019/12/05 데일리 회의 기록 작성 시 상단에 하기의 이미지와 같은 설정 추가

```
layout: post      
title: 2019/12/05 데일리
comments: true		
categories : [Project/Daily]	
tags: [Daily]	
author: jungeunlee95		
userImage: /assets/user-img/jungeun.png   
```

📌 `layout:` 레이아웃 설정                 

📌 `title:` 글 제목 설정         

📌 `comments:` 댓글 기능 사용 여부         

📌 `categories:` 카테고리 설정       

📌 `tags:` 태그 설정    

📌 `author:` 작성자 설정         

📌 `userImage:` 작성자 사진 설정         

​     

<br>

<br>

<br>

