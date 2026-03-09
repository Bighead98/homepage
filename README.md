# 연구자 개인 홈페이지

연구자를 위한 개인 홈페이지 템플릿입니다. 순수 HTML/CSS/JavaScript로 제작되어 별도의 빌드 도구 없이 바로 사용할 수 있습니다.

## 주요 기능

- **7개 섹션**: 소개, 학력/경력, 연구 분야, 논문/출판물, 프로젝트, 수상, 연락처
- **반응형 디자인**: 모바일, 태블릿, 데스크톱 지원
- **다크모드**: 시스템 설정 자동 감지 + 수동 토글
- **스크롤 애니메이션**: Intersection Observer 기반 fade-in 효과
- **고정 네비게이션**: 스크롤 시 현재 섹션 자동 하이라이트

## 파일 구조

```
├── index.html          메인 HTML
├── css/
│   └── style.css       스타일시트
├── js/
│   └── main.js         인터랙션 스크립트
├── assets/
│   └── profile.jpg     프로필 사진 (직접 추가)
└── README.md           이 파일
```

## 사용법

### 1. 내용 수정

`index.html`을 열어 placeholder 텍스트를 본인의 정보로 교체하세요:

- 이름, 직함, 소속
- 학력 및 경력 사항
- 연구 분야 설명
- 논문 목록 및 링크
- 프로젝트 정보
- 수상 내역
- 연락처 및 소셜 링크

### 2. 프로필 사진 추가

`assets/` 폴더에 `profile.jpg` 파일을 넣고, `index.html`에서 프로필 이미지 부분을 수정하세요:

```html
<!-- 이 부분을 찾아서 -->
<div class="profile-placeholder">...</div>

<!-- 아래처럼 교체 -->
<img src="assets/profile.jpg" alt="프로필 사진" style="width:180px;height:180px;border-radius:50%;object-fit:cover;">
```

### 3. 로컬 미리보기

아무 웹 브라우저에서 `index.html`을 더블클릭하면 바로 확인할 수 있습니다.

VS Code를 사용한다면 Live Server 확장을 설치하여 실시간 미리보기가 가능합니다.

## GitHub Pages 배포 방법

### 1단계: Git 초기화 및 커밋

```bash
cd 홈페이지
git init
git add .
git commit -m "Initial commit: 연구자 개인 홈페이지"
```

### 2단계: GitHub 저장소 생성

1. [github.com](https://github.com)에서 새 저장소(repository)를 생성합니다
2. 저장소 이름을 `username.github.io`로 설정하면 `https://username.github.io`로 접근 가능합니다
3. 일반 이름(예: `homepage`)으로 설정하면 `https://username.github.io/homepage`로 접근됩니다

### 3단계: Push 및 배포

```bash
git remote add origin https://github.com/username/username.github.io.git
git branch -M main
git push -u origin main
```

### 4단계: GitHub Pages 활성화

1. GitHub 저장소 > **Settings** > **Pages**
2. **Source**에서 `Deploy from a branch` 선택
3. **Branch**에서 `main` / `/ (root)` 선택 후 **Save**
4. 1~2분 후 배포 완료

## 커스터마이징

### 색상 변경

`css/style.css` 상단의 CSS 변수를 수정하면 전체 색상 테마를 변경할 수 있습니다:

```css
:root {
  --color-accent: #2563eb;    /* 메인 강조 색상 */
  --color-primary: #1b2a4a;   /* 제목/로고 색상 */
}
```

### 폰트 변경

`index.html`의 Google Fonts 링크와 `css/style.css`의 `--font-sans` 변수를 수정하세요.

## 라이선스

자유롭게 수정하여 사용하세요.
