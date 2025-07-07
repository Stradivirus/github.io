# My GitHub Blog

Jekyll을 사용한 GitHub Pages 블로그입니다.

## 로컬에서 실행하기

1. Ruby와 Bundler 설치
2. 의존성 설치:
   ```bash
   bundle install
   ```
3. 로컬 서버 실행:
   ```bash
   bundle exec jekyll serve
   ```
4. 브라우저에서 `http://localhost:4000` 접속

## 새 포스트 작성하기

`_posts` 폴더에 `YYYY-MM-DD-title.md` 형식으로 파일을 생성하고, 다음 형식으로 작성:

```markdown
---
layout: post
title: "포스트 제목"
date: YYYY-MM-DD HH:MM:SS +0900
categories: [category1, category2]
tags: [tag1, tag2]
author: "작성자명"
---

포스트 내용을 여기에 작성하세요.
```

## 파일 구조

- `_config.yml`: Jekyll 설정 파일
- `_layouts/`: 레이아웃 템플릿
- `_posts/`: 블로그 포스트
- `assets/`: CSS, 이미지 등 정적 파일
- `index.html`: 메인 페이지
- `about.md`: 소개 페이지
- `posts.md`: 모든 포스트 목록