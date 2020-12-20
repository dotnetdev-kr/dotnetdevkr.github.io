![CI](https://github.com/dotnetdev-kr/dotnetdev-kr.github.io/workflows/CI/badge.svg)

# dotnetdev-kr.github.io

닷넷데브의 웹사이트 저장소 입니다. [Hugo](https://gohugo.io/)로 만들어 졌습니다.  
`main` 브랜치에 수정사항을 커밋하면, GitHub Actions 를 통해 자동으로 `gh-pages` 브랜치로 빌드된 파일이 푸시됩니다.

[웹사이트 방문](https://dotnetdev-kr.github.io)

## 블로그 글 작성하기

[Hugo CLI](https://gohugo.io) 를 먼저 설치합니다. 이후 본 저장소를 서브모듈까지 로컬로 복제합니다.

```bash
git clone --recursive https://github.com/dotnetdev-kr/dotnetdev-kr.github.io
```

블로그 폴더로 간 다음, 아래 명령으로 새 블로그 포스트를 생성합니다.

```bash
hugo new --kind blog blog/YYYY-MM-DD-Title.md
# 예시 hugo new --kind blog blog/2020-11-02-welcome-to-dotnetdev-kr.md
```

아래와 같은 내요의 파일이 생성됩니다. `+++`로 감싸진 부분은 TOML Front matter 입니다, 여기에 포스트 메타데이터가 들어갑니다.
`#`으로 시작하는 주석을 참고하여 정보를 작성합니다.
```toml
+++
title = "" # 제목
description = "" #짧은 설명
date = 2020-11-03T00:27:56+09:00 # 작성 일시
weight = 20
draft = false # 게시 여부
[[author]] # 작성자 정보
    name = "" # 이름
    email = "" # 이메일
    bio = "" # 소개
    linklabel = "" # 개인 링크 제목
    linkurl = "" # 개인 링크 주소
+++
```
하나의 게시물에 작성자가 여러명인 경우, 아래와 같이 작성합니다.
```toml
+++
title = "" # 제목
description = "" #짧은 설명
date = 2020-11-03T00:27:56+09:00 # 작성 일시
weight = 20
draft = false # 게시 여부
[[author]] # 작성자 정보
    name = "" # 이름
    email = "" # 이메일
    bio = "" # 소개
    linklabel = "" # 개인 링크 제목
    linkurl = "" # 개인 링크 주소
[[author]] # 작성자1 정보
    name = "" # 이름
    email = "" # 이메일
    bio = "" # 소개
    linklabel = "" # 개인 링크 제목
    linkurl = "" # 개인 링크 주소
+++
```
이후 이어지는 내용은 Markdown 문법에 따라 작성합니다.
