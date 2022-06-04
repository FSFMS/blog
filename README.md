# FSFMS 블로그

## 프로젝트 셋팅

node.js 설치
```shell
$ brew install node@17
$ npm install -g yarn
$ npm install -g hexo-cli
```

패키지 설치
```shell
$ yarn install
```

## 블로그 포스트 생성

포스트 생성 전 자신의 닉네임으로 된 폴더를 `/source/_post/` 폴더에 만들어주세요.

포스트 생성을 위해 아래 명령어를 입력해주세요.

```shell
$ hexo new post "포스트 명"
```

위 명령어를 실행하면 `/source/_post/` 폴더에 포스트가 생성됩니다.
`포스트 명.md`와 `/포스트 명/` 폴더가 생성됩니다. md 파일은 포스트가 작성될 마크다운 파일이고, 폴더는 해당 포스트에 사용되는 사진 등의 파일이 저장되는 폴더입니다.  
위의 마크다운 파일과 폴더를 자신의 폴더로 이동하면 포스트 생성이 완료되었습니다.

## 포스트 작성

위에서 생성한 빈 포스트 파일의 가장 상단엔 아래와 같이 기본 정보가 입력되어 있습니다. 
```markdown
---
title: Hello World
tags: 
date: 2022-05-31
toc: true
category: 
---
```

1. title
    - 생성 할 때 입력한 포스트의 제목입니다. 여기서 변경하면 블로그에 반영됩니다.
    - 제목짓는 규칙이 필요할것 같네요.
2. tags
   - [hello, world, algorithm]과 같이 배열에 문자열을 넣어서 태그를 넣을 수 있습니다.
   - 태그는 블로그의 태그 메뉴에서도 확인 가능합니다.
   - 태그의 작명도 규칙이 필요할것 같네요. 모두 소문자로 작성한다던지...
3. date
   - 포스트가 생성된 날짜입니다.
   - 이건 그냥 자동생성되니 건들지 않아도 좋지만, 포스트 생성일과 업로드한 날짜가 다르다면 수정해도 괜찮습니다.
4. toc
   = 포스팅의 목차 여부입니다. 그냥 냅두세요.
5. category
   - 카테고리를 입력할수 있습니다.
   - 태그처럼 따옴표 없는 문자열을 입력해서 카테고리를 지정 할수 있습니다.

나머지는 마크다운 문법을 이용해서 자유롭게 작성하면 됩니다.

포스트를 그냥 작성하게되면 모든 포스팅 내용이 목록에 나타나게 됩니다. 포스팅 초반의 미리보기 할 부분 바로 아랫줄에 아래처럼 입력해주세요.
```markdown
More info: [Generating](https://hexo.io/docs/generating.html)

<!-- more --> 

### Deploy to remote sites
```
포스팅 목록에선 자세히 보기로 나머지 포스팅이 감춰집니다.

## 로컬에서 확인

```shell
$ hexo serve
```
웹 브라우저에서 [로컬주소](localhost:4000/readme/) 로 접속하면 확인 가능

## 자동배포

```shell
$ hexo deploy --generate
```

배포가 제대로 되지 않았을경우
```shell
$ hexo clean
$ hexo deploy --generate
```