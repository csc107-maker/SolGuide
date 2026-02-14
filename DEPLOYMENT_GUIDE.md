# 🚀 무료 호스팅 배포 가이드

## 📌 개요

도메인 없이 무료로 웹사이트를 호스팅하고 운영하는 방법을 안내합니다.
3가지 추천 서비스 중 선택하세요!

---

## 🏆 추천 서비스 비교

| 서비스 | 장점 | 단점 | 난이도 |
|--------|------|------|--------|
| **Netlify** | 가장 간단, Drag&Drop | - | ⭐ (최고) |
| **GitHub Pages** | 무료, 안정적, Git 연동 | Git 필요 | ⭐⭐ |
| **Vercel** | 빠름, 자동 배포 | - | ⭐⭐ |

---

## 방법 1: Netlify (가장 추천!) ⭐

### 특징
- **드래그 앤 드롭** 방식 (가장 쉬움)
- Git 필요 없음
- 자동 HTTPS
- 무료 도메인 제공 (your-site.netlify.app)

### 단계별 설정

#### 1단계: 프로젝트 폴더 압축

**Windows:**
1. 프로젝트 폴더 우클릭
2. "보내기" > "압축(ZIP) 폴더"
3. `solar-guide.zip` 생성

**Mac:**
1. 프로젝트 폴더 우클릭
2. "압축하기"
3. `solar-guide.zip` 생성

#### 2단계: Netlify 가입

1. https://www.netlify.com/ 접속
2. "Sign up" 클릭
3. GitHub, GitLab, 이메일 중 선택
4. 무료 플랜 선택

#### 3단계: 사이트 배포

1. Netlify 대시보드에서 **"Add new site"** 클릭
2. **"Deploy manually"** 선택
3. 압축한 `solar-guide.zip` 파일을 드래그 앤 드롭
   
   또는
   
   압축 해제한 **폴더 전체**를 드래그 앤 드롭

4. 업로드 완료 대기 (1-2분)

#### 4단계: 사이트 확인

- 자동으로 URL 생성: `https://random-name-12345.netlify.app`
- 클릭해서 사이트 확인!

#### 5단계: 사이트 이름 변경 (선택)

1. "Site settings" 클릭
2. "Change site name" 클릭
3. 원하는 이름 입력 (예: `solar-guide`)
4. 새 URL: `https://solar-guide.netlify.app`

---

### 📝 파일 수정 후 재배포

1. 로컬에서 파일 수정
2. Netlify 대시보드 > "Deploys" 탭
3. 수정된 파일들을 다시 드래그 앤 드롭
4. 자동으로 업데이트!

---

## 방법 2: GitHub Pages

### 특징
- GitHub과 연동
- 버전 관리 가능
- 무료 도메인 (username.github.io/repo-name)

### 단계별 설정

#### 1단계: GitHub 계정 만들기

1. https://github.com/ 접속
2. "Sign up" 클릭
3. 계정 생성

#### 2단계: 저장소(Repository) 만들기

1. 오른쪽 상단 "+" > "New repository" 클릭
2. Repository name: `solar-guide`
3. Public 선택
4. "Create repository" 클릭

#### 3단계: 파일 업로드

**방법 A: 웹 인터페이스 (쉬움)**

1. "uploading an existing file" 링크 클릭
2. 모든 HTML, CSS, JS 파일 드래그
3. "Commit changes" 클릭

**방법 B: GitHub Desktop (권장)**

1. [GitHub Desktop](https://desktop.github.com/) 다운로드
2. 설치 후 GitHub 계정 로그인
3. "Clone a repository" > 위에서 만든 저장소 선택
4. 로컬 폴더에 프로젝트 파일 복사
5. GitHub Desktop에서 "Commit to main" > "Push origin"

#### 4단계: GitHub Pages 활성화

1. 저장소 페이지에서 "Settings" 클릭
2. 왼쪽 메뉴 "Pages" 클릭
3. Source: "Deploy from a branch"
4. Branch: `main` 선택
5. Folder: `/ (root)` 선택
6. "Save" 클릭

#### 5단계: 사이트 확인 (2-3분 후)

- URL: `https://your-username.github.io/solar-guide/`

---

### 📝 파일 수정 후 재배포

1. 로컬에서 파일 수정
2. GitHub Desktop에서 "Commit" > "Push"
3. 자동으로 업데이트! (1-2분 소요)

---

## 방법 3: Vercel

### 특징
- 매우 빠른 배포
- 자동 HTTPS
- 무료 도메인 (your-site.vercel.app)

### 단계별 설정

#### 1단계: Vercel 가입

1. https://vercel.com/ 접속
2. "Sign Up" 클릭
3. GitHub/GitLab/이메일 선택
4. 무료 플랜 (Hobby) 선택

#### 2단계: 사이트 배포

**방법 A: Drag & Drop (쉬움)**

1. 대시보드에서 "Add New" > "Project" 클릭
2. "Browse" 클릭 또는 폴더 드래그
3. 프로젝트 폴더 선택
4. "Deploy" 클릭

**방법 B: GitHub 연동 (자동 배포)**

1. GitHub에 저장소 만들기 (위 GitHub Pages 참고)
2. Vercel에서 "Import Git Repository"
3. GitHub 저장소 선택
4. "Deploy" 클릭
5. 이후 GitHub에 푸시하면 자동 배포!

#### 3단계: 사이트 확인

- 자동 URL: `https://solar-guide-xxxxx.vercel.app`

---

## 🔧 공통 설정 작업

배포 후 모든 서비스에서 해야 할 일:

### 1. Google Analytics 코드 추가

배포 **전에** HTML 파일에 Analytics 코드 추가하세요.
(자세한 내용은 `GOOGLE_ANALYTICS_GUIDE.md` 참고)

### 2. 블로그 URL 확인

- `business.html`에 네이버 블로그 링크 추가됨 ✅
- URL: https://blog.naver.com/ecosolution1218

### 3. 연락처 확인

- 전화번호: 070-5159-5119 ✅

### 4. 파비콘 확인

- `favicon.svg` 파일이 루트 폴더에 있는지 확인

---

## 📱 파일 수정 및 업데이트 방법

### Netlify
1. 파일 수정
2. Netlify 대시보드 > Deploys
3. 수정된 파일 드래그 앤 드롭

### GitHub Pages
1. 파일 수정
2. GitHub Desktop에서 Commit > Push
3. 자동 업데이트 (1-2분)

### Vercel
1. 파일 수정
2. GitHub에 푸시 (GitHub 연동 시)
   또는 Vercel CLI 사용

---

## 🎨 도메인 연결 (나중에)

무료 도메인으로 시작 → 나중에 원하면 도메인 구매

### 도메인 구매처
- [가비아](https://www.gabia.com/): 연 1만~2만 원
- [Namecheap](https://www.namecheap.com/): 연 $10-15
- [Cloudflare](https://www.cloudflare.com/): 연 $10

### 연결 방법
각 호스팅 서비스 문서 참고:
- [Netlify 도메인 연결](https://docs.netlify.com/domains-https/custom-domains/)
- [GitHub Pages 도메인 연결](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
- [Vercel 도메인 연결](https://vercel.com/docs/concepts/projects/domains)

---

## ✅ 배포 체크리스트

배포 전 확인사항:

- [ ] 모든 HTML 파일에 Google Analytics 코드 추가
- [ ] 블로그 URL 업데이트 (https://blog.naver.com/ecosolution1218)
- [ ] 연락처 정보 확인 (070-5159-5119)
- [ ] 파비콘 파일 포함 (favicon.svg)
- [ ] 모든 링크 작동 확인
- [ ] 모바일에서 테스트

배포 후 확인사항:

- [ ] 웹사이트 접속 확인
- [ ] 모든 페이지 작동 확인
- [ ] 계산기 기능 테스트
- [ ] 폼 제출 테스트
- [ ] Google Analytics 설치 확인

---

## 🆘 문제 해결

### 페이지가 안 보여요
- 2-3분 기다려보세요 (배포 시간)
- 캐시 삭제: `Ctrl + Shift + Delete`
- 시크릿 모드로 열기

### 이미지/CSS가 안 보여요
- 파일 경로 확인 (`/css/style.css` → `css/style.css`)
- 모든 파일이 업로드되었는지 확인

### 404 에러가 나요
- index.html이 루트 폴더에 있는지 확인
- 파일명 대소문자 확인 (Index.html ❌, index.html ✅)

---

## 🎯 추천 배포 순서

**1일차: Netlify로 빠른 배포**
- 가장 쉽고 빠름
- Drag & Drop으로 5분 완성

**1주차: 블로그와 연동**
- 블로그에 웹사이트 링크 추가
- 웹사이트에서 블로그로 트래픽 유도

**1개월차: GitHub Pages로 마이그레이션 (선택)**
- 버전 관리 필요 시
- 더 전문적인 워크플로우

---

## 📊 성과 추적

배포 후 1주일 뒤:
- Google Analytics에서 방문자 확인
- 인기 페이지 파악
- 유입 경로 분석

배포 후 1개월 뒤:
- 콘텐츠 업데이트
- SEO 최적화
- 블로그 글 추가

---

## 💡 다음 단계

1. ✅ **배포 완료** (Netlify/GitHub Pages/Vercel)
2. ✅ **Google Analytics 설치**
3. ✅ **블로그에 웹사이트 링크 추가**
4. 📝 **블로그 포스팅 작성**
   - "EPC 파트너십 수익 모델"
   - "2026년 태양광 금융지원 총정리"
   - "발전소 매매 실전 가이드"
5. 📈 **SEO 최적화**
   - Google Search Console 등록
   - 네이버 웹마스터 도구 등록

---

**축하합니다! 🎉**
이제 누구나 접근 가능한 전문 웹사이트를 보유하게 되었습니다!

궁금한 점이 있으면 각 서비스의 문서를 참고하세요:
- [Netlify 문서](https://docs.netlify.com/)
- [GitHub Pages 문서](https://docs.github.com/en/pages)
- [Vercel 문서](https://vercel.com/docs)
