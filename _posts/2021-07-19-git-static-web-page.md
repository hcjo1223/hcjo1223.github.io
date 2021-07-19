---
title: "GitHub Pages를 이용한 정적 웹 페이지 호스팅 하기"
categories:
  - Blog
tags:
  - Blog
  - 블로그
  - github-page
---

# Github Pages란?

> 깃허브(Git Hub)는 깃(소프트웨어 개발에서 여러 명의 사용자들 간에 해당 파일들의 작업을 조율하기 위한 분산 버전 관리 시스템)을 좀 더 편하게 이용하도록 만든 깃 서버 웹 호스팅 서비스이고 오픈소스 소프트웨어의 중심지(hub) 역할을 하면서 오픈소스 프로젝트가 널리 퍼지는 데 크게 기여하고 있는 서비스입니다.  
> 깃허브 페이지(GitHub Pages)는 이러한 깃허브에서 제공하는 정적 사이트 호스팅 서비스로 일반적인 HTML 콘텐츠를 지원하는 것 외에도 인기있는 정적 사이트 생성기인 Jekyll을 지원합니다.

<br>

# 정적 웹 페이지란?

<img src="/assets/images/2021-07-19-git-static-web-page/static_web_page.png">

> 정적 웹 페이지는 웹 서버에 미리 저장된 파일들(HTML, CSS, Javascript 파일 등)이 그대로 사용자에게 전달되어 보여지는 웹 페이지이다. 즉, 웹 서버가 정적 웹 페이지에 대한 요청을 받은 경우 서버는 추가적인 처리 과정 없이 클라이언트에게 응답을 보냅니다. 예를 들어 회사나 개인의 소개 페이지가 정적 웹 페이지의 좋은 예시입니다.

<br><br><br>

# 호스팅 과정

## Github 가입하기

* <a href="https://github.com/" target="_blank">https://github.com/</a>

<img src="/assets/images/2021-07-19-git-static-web-page/github_sign_in.png">

> 여기서 사용자이름(Username)은 이후 생성되는 깃허브 페이지 사이트의 도메인이 됩니다. (**_사용자이름_**.github.io)

<br><br>

## 저장소 생성



![저장소 생성 메뉴](/assets/images/2021-07-19-git-static-web-page/github_menu.png)

* <a href="https://github.com/new" target="_blank">https://github.com/new</a>

우측 상단의 “+” 아이콘을 누른 후 **New repository** 버튼을 누르거나, 위 링크로 들어가자

<img src="/assets/images/2021-07-19-git-static-web-page/github_createrepo.png">

> <strong>-Repository name : 프로젝트 이름</strong>   
> <em>("github아이디.github.io"로 저장소를 만들면, 별도의 설정 없이 이 블로그와 같은 "https://github아이디.github.io/"의 형태로 웹 페이지가 생성된다)</em>
> 
> <strong>-Description : 프로젝트 설명</strong>   
> 
> <strong>-Public/Private : 전체공개/비공개 설정</strong>   
> <em>(Private으로 설정하면, Github 호스팅 서비스를 사용할 수 없다)</em>

<br><br>

## 프로젝트 업로드

* <em style="color:gray;">git CLI(터미널을 이용하는 방식)를 통해 프로젝트를 github 상에 업로드할 수 있지만, git/github 사용에 익숙하지 않은 분들을 고려하여 github에서 직접 파일을 업로드하는 방식을 선택했다<em>

<br>

<img src="/assets/images/2021-07-19-git-static-web-page/github_upload.png">

> 1. <strong style="color:#0366d6">uploading an existing file</strong> 클릭   
> 2. 파일 드래그 or 파일 선택을 통해 파일들을 업로드   
> 3. <strong style="color:#2ea44f">Commit changes</strong> 클릭

<br><br>

## Github Pages 설정

브라우저로 “https://github.com/**_사용자이름_**/**_저장소이름_**/settings” 에 접속을 하면 저장소 설정을 하실 수 있습니다.

<img src="/assets/images/2021-07-19-git-static-web-page/github_page.png">

<br><br>

하단에 있는 **GitHub Pages > Source**에 **None**으로 된 선택창을 **master**로 변경 후 Save

> 호스팅에 소요되는 0~2분 후에 링크를 들어가면, 웹 페이지가 정상적으로 작동하게 된다.
> https://**_사용자이름_**.github.io/**_저장소이름_**/

<br><br>

## GitHub Pages URL 뒤에 저장소 이름없이 생성하기
repository생성후 page를 활성화하면  
“https://**_사용자이름_**.github.io/**_저장소이름_**/” 으로 사이트가 생성된다.  
“https://**_사용자이름_**.github.io/” 주소로 바로 연결되게 하고 싶으면 깃허브 저장소 생성 시 Repository name에 “**_사용자이름_**.github.io”로 생성을 하면 된다.
> “**_사용자이름_**.github.io”로 저장소를 생성할 경우 별도로 깃허브 페이지 활성 설정을 하지 않아도 사이트가 생성된다.

<br><br><br>

## GitHub Pages 의 제한 사항

> GitHub Pages 소스 저장소의 권장 제한은 1GB입니다.  
게시 된 GitHub 페이지 사이트는 1GB를 초과 할 수 없습니다.  
GitHub 페이지 사이트의 대역폭 제한은 한 달에 100GB입니다.  
GitHub 페이지 사이트의 builds 제한은 시간당 10회 입니다.

## 유사 서비스

깃허브 페이지와 같이 무료로 정적 웹 사이트 호스팅을 제공하는 서비스들이 많이 있다.

> -   [Gitlab Pages](https://about.gitlab.com/stages-devops-lifecycle/pages/)
> -   [Netlify](https://www.netlify.com/)
> -   [Neocities](https://neocities.org/)

<br><br><br>

#### 참고 자료
* <a href="https://ko.wikipedia.org/wiki/%EA%B9%83%ED%97%88%EB%B8%8C" target="_blank">위키백과 - 깃허브</a>
* <a href="https://titus94.tistory.com/4" target="_blank">Titus `열정의 공간 블로그</a>
* <a href="https://hogni.tistory.com/75" target="_blank">빠른손김참치 블로그</a>
* <a href="https://wepplication.github.io/programming/github-pages/">WEPPLICATION 블로그</a>