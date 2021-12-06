# 20213099 홍성목

## **1st.** Start Jekyll

[Jekyll 공식 사이트](https://jekyllrb-ko.github.io/)에서 Jekyll을 설치한다.  
설치가 완료되면 `jekyll -v` 명령어를 통해 잘 설치되었는지 확인한다.  

## **2nd.** Fork Lanyon

블로그의 기초 작업을 빠르게 수행하기 위해 **[Lanyon](https://github.com/poole/lanyon)** 테마의 원격 저장소를 **fork**한다.  
가져온 저장소의 이름을 ssb2ss.github.io로 변경한다.  
블로그의 설정을 상황에 맞게 다음과 같이 작성한다.  
```yml
# Setup
title:               ssb2ss
tagline:             'Sungmok Hong'
description:         '20213099'
url:                 https://ssb2ss.github.io
#baseurl:             ''
paginate:            5
permalink:           pretty

# About/contact
author:
  name:              ssb2ss
  url:               https://ssb2ss.github.io
  email:             ssb2ss@kookmin.ac.kr

# Gems
plugins:
  - jekyll-paginate

# Custom vars
version:             1.1.0
google_analytics_id: #UA-XXXX-Y
```
원격 저장소에 업로드한다.
```
git add _config.yml
git commit -m "Init blog lanyon"
git push origin master
```

## **3rd.** Upload first post

나만의 포스트를 작성하기 위해 먼저 **[Lanyon](https://github.com/poole/lanyon)** 테마에 기본으로 들어있는 더미 포스트를 삭제한다.  
`_posts/2021-11-25-First_Post.md` 파일을 만들어 다음과 같이 작성한다.
```
---
layout: post
title: "First Post"
date:   2021-11-25 20:35:00 +0900
categories: jekyll update
---

# First Post

- 20213099
- Sungmok Hong
```
글을 올리는 것에 의의가 있는 것이기 때문에 내용은 간단하다.  
원격 저장소에 업로드한다.
```
git add _posts/2021-11-25-First_Post.md
git commit -m "Add first post"
git push origin master
```

## **4th.** Add comments

[Disqus](https://disqus.com/) 서비스를 이용해 댓글 기능을 추가한다.
사이트 내에서 세팅을 마친 뒤, `_config.yml`에 다음과 같은 key-value를 추가한다.  
```yml
comment:
  provider: "disqus"
  disqus:
    shortname: "ssb2ss"
```
이후 Universal Code를 `_layouts/post.html`에 추가한다.
```html
{% if page.comments %}
<h2>Commnets</h2>
<div id="disqus_thread"></div>
<script>
    /**
    *  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
    *  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables    */
    let PAGE_URL = "{{site.url}}{{page.url}}"
    let PAGE_IDENTIFIER = "{{page.url}}"
    var disqus_config = function () {
    this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
    this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
    };
    (function() { // DON'T EDIT BELOW THIS LINE
    var d = document, s = d.createElement('script');
    s.src = 'https://ssb2ss.disqus.com/embed.js';
    s.setAttribute('data-timestamp', +new Date());
    (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
{% endif %}
```
이제 댓글을 허용하고 싶은 포스트에 `comments: true`를 추가한다.

## **5th.** Upload topic post

특강에 다뤄졌던 내용 중 Markdown 문법에 관련된 글에 대해 작성하기로 한다.  
작성한 포스트는 [여기](https://ssb2ss.github.io/jekyll/update/2021/12/06/About-Markdown/)에서 확인 가능하다.
