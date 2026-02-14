# ✅ Solar Guide → solguide.net 배포 완벽 가이드
## GitHub Desktop 사용 (초보자용 · 5분 완성)

---

## 📦 1단계: GitHub Desktop 설치 (2분)

### 다운로드 & 설치
1. 브라우저에서 https://desktop.github.com/ 접속
2. **"Download for Windows"** 클릭 (또는 Mac)
3. 다운로드된 파일 실행 → 설치 완료

### 로그인
1. GitHub Desktop 실행
2. **"Sign in to GitHub.com"** 클릭
3. 브라우저가 열리면 GitHub 계정으로 로그인
4. **"Authorize desktop"** 클릭

---

## 📂 2단계: solguide.net 레포지토리 클론 (1분)

### 클론하기
1. GitHub Desktop에서 **File** → **Clone repository** 클릭
2. **GitHub.com** 탭에서 목록 확인
3. **"solguide"** 또는 **"csc107"** 같은 이름의 레포지토리 찾기
4. **Local path**(저장 위치) 설정:
   ```
   C:\Users\사용자이름\Documents\solguide-net
   ```
5. **Clone** 버튼 클릭

---

## 🗑️ 3단계: 기존 파일 삭제 (1분)

### 폴더 열기
1. GitHub Desktop에서 **Repository** → **Show in Explorer** 클릭
2. 폴더가 열림

### 파일 삭제 ⚠️ 중요
1. **숨김 파일 보기 설정**:
   - 파일 탐색기 → **보기** 탭 → **숨김 항목** 체크
2. **.git 폴더를 제외한** 모든 파일·폴더 선택 → 삭제
   - ❌ 삭제할 것: index.html, package.json, src/, public/ 등 **모든 파일**
   - ✅ 남길 것: **.git** 폴더만 (숨김 폴더)

---

## 📥 4단계: Solar Guide 파일 복사 (1분)

### 파일 복사
1. **Solar Guide 프로젝트 폴더** 열기
2. **모든 파일 선택** (Ctrl + A):
   ```
   ✅ index.html
   ✅ calculator.html
   ✅ finance.html
   ✅ business.html
   ✅ contractors.html
   ✅ equipment.html
   ✅ diy.html
   ✅ investment.html
   ✅ favicon.svg
   ✅ css/ (폴더)
   ✅ js/ (폴더)
   ✅ README.md
   ✅ DEPLOYMENT_GUIDE.md
   ✅ GOOGLE_ANALYTICS_GUIDE.md
   ✅ 기타 모든 파일
   ```
3. **복사** (Ctrl + C)
4. **클론한 레포지토리 폴더**로 이동
5. **붙여넣기** (Ctrl + V)

---

## 🚀 5단계: 커밋 & 푸시 (1분)

### GitHub Desktop에서 배포
1. GitHub Desktop으로 돌아가기
2. 왼쪽 패널에 **변경된 파일 목록** 표시됨 (빨간색/초록색)
3. 왼쪽 하단 **Summary** 입력창에 작성:
   ```
   솔라가이드 웹사이트 배포
   ```
4. **Commit to main** 버튼 클릭 (파란색)
5. 상단 중앙의 **Push origin** 버튼 클릭 (↑ 아이콘)

---

## ⏰ 6단계: 자동 배포 대기 (2분)

### Netlify 자동 빌드
1. GitHub에 푸시되면 **Netlify가 자동으로 감지**
2. **1~3분 대기** (빌드 시간)
3. Netlify 대시보드 → **Deploys** 탭에서:
   - **"Building"** → **"Published"** 상태 변경 확인

---

## ✅ 7단계: 배포 확인

### 웹사이트 접속
1. 브라우저 시크릿 모드 열기 (Ctrl + Shift + N)
2. **https://solguide.net** 접속
3. **전체 페이지 확인**:

   - [ ] **홈페이지** → 히어로, 통계 카드, 4개 서비스 박스
   - [ ] **/calculator.html** → 수익 계산기 작동
   - [ ] **/finance.html** → 금융지원 4개 탭
   - [ ] **/business.html** → 3개 비즈니스 모델 + 블로그 링크
   - [ ] **/contractors.html** → 시공업체 체크리스트
   - [ ] **/equipment.html** → 기자재 비교표
   - [ ] **/diy.html** → DIY 6단계 아코디언
   - [ ] **/investment.html** → 투자 정보, 주식 티커
   - [ ] **모바일 반응형** (F12 → 디바이스 도구 모음)
   - [ ] **파비콘** 표시

---

## 🔧 문제 해결

### Q1: GitHub Desktop에 레포지토리가 안 보여요
**해결**: 
1. GitHub 웹사이트(https://github.com/) 접속 → 로그인
2. 레포지토리 찾기 (solguide 또는 csc107)
3. 레포지토리 페이지에서 **Code** → **HTTPS URL 복사**
4. GitHub Desktop → **File** → **Clone repository** → **URL** 탭
5. 복사한 URL 붙여넣기

### Q2: .git 폴더가 안 보여요
**해결**: 
- Windows: 파일 탐색기 → **보기** → **숨김 항목** 체크
- Mac: Finder → Cmd + Shift + . (점)

### Q3: Push가 안 돼요 (Authentication failed)
**해결**: 
1. GitHub Desktop → **File** → **Options** → **Accounts**
2. **Sign out** → 다시 로그인

### Q4: Netlify 빌드 실패 (Build failed)
**해결**: 
1. Netlify 대시보드 → **Deploys** → 실패한 배포 클릭
2. **Deploy log** 확인
3. 에러 메시지 복사 후 문의

### Q5: 배포 후에도 기존 사이트가 보여요
**해결**: 
- 브라우저 캐시 삭제: **Ctrl + Shift + R** (강력 새로고침)
- 시크릿 모드로 확인
- 10분 대기 후 재확인

---

## 🎉 배포 완료 후 작업

### 즉시 (10분)
1. ✅ **Google Analytics 설치**
   - https://analytics.google.com/ 접속
   - 측정 ID 받기 (G-XXXXXXXXXX)
   - 모든 HTML 파일 `<head>`에 GA 스크립트 추가
   - 다시 커밋·푸시

2. ✅ **네이버 블로그 포스팅**
   - 제목: "태양광 사업 종합 정보 사이트 '솔라가이드' 오픈!"
   - 내용: 사이트 소개 + https://solguide.net 링크
   - 해시태그: #태양광 #태양광발전 #태양광사업 #수익계산

### 1주일 내
1. ✅ **SEO 등록**
   - Google Search Console: https://search.google.com/search-console
   - 네이버 웹마스터 도구: https://searchadvisor.naver.com/

2. ✅ **블로그 글 작성** (주 2~3회)
   - "2026년 태양광 금융지원 총정리"
   - "100kW 태양광 실제 수익 계산 사례"
   - "EPC 파트너십으로 수익 극대화하는 법"

---

## 📞 추가 지원

- GitHub Desktop 문서: https://docs.github.com/en/desktop
- Netlify 문서: https://docs.netlify.com/
- 문제 발생 시: 에러 메시지 스크린샷 공유

---

**작성일**: 2026-02-14  
**버전**: 1.1  
**소요 시간**: 총 5분
