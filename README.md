# JH.LOG

Astro + GitHub Pages용 최소 기술 블로그 스타터입니다.

## 1. 수정할 곳

`astro.config.mjs`

```js
site: 'https://YOUR_GITHUB_USERNAME.github.io'
```

`src/components/Header.astro`

```js
href: 'https://github.com/YOUR_GITHUB_USERNAME'
```

## 2. 로컬 실행

```bash
npm install
npm run dev
```

## 3. GitHub Pages 배포

저장소가 `YOUR_GITHUB_USERNAME.github.io`라면 현재 설정 그대로 사용할 수 있습니다.

GitHub 저장소에서:

1. Settings → Pages
2. Source를 **GitHub Actions**로 선택
3. `main` 브랜치에 push

`.github/workflows/deploy.yml`이 Astro를 빌드하고 GitHub Pages에 배포합니다.

## 4. 글 추가

현재 샘플 글은 모두 제거되어 있습니다. 이후 `src/pages/posts/` 아래에 `.md` 또는 `.astro` 파일을 추가하면 됩니다.

예: `src/pages/posts/kmp.md` → `/posts/kmp`

> 글 목록 자동 생성, 태그, 시리즈, TOC가 필요해지면 Astro Content Collections 구조로 확장하는 것을 권장합니다.

## 일반 저장소를 Pages로 쓰는 경우

저장소가 `blog`라면 `astro.config.mjs`에 `base`를 추가합니다.

```js
export default defineConfig({
  site: 'https://YOUR_GITHUB_USERNAME.github.io',
  base: '/blog',
});
```
