# GitHub를 통한 Solguide.net 배포 가이드

## 🎯 목표
GitHub Desktop을 사용하여 Solar Guide 웹사이트를 solguide.net에 배포합니다.

---

## 📋 사전 준비 (5분)

### 1. GitHub Desktop 설치
- **다운로드**: https://desktop.github.com/
- 설치 후 GitHub 계정으로 로그인

### 2. 기존 레포지토리 확인
1. GitHub 웹사이트(https://github.com/)에 로그인
2. 상단 오른쪽 프로필 → **Your repositories** 클릭
3. `solguide.net` 또는 `tanstack-chat` 관련 레포지토리 찾기

---

## 🚀 배포 단계

### STEP 1: 레포지토리 클론 (복제)

1. **GitHub Desktop** 실행
2. **File** → **Clone repository** 클릭
3. 목록에서 **solguide.net 레포지토리** 선택
4. **Local path**(저장 위치) 지정 후 **Clone** 클릭
   - 예: `C:\Users\사용자이름\Documents\solguide-net`

---

### STEP 2: 기존 파일 백업 및 삭제

1. 클론한 폴더 열기 (GitHub Desktop에서 **Repository** → **Show in Explorer**)
2. **모든 기존 파일 선택** → **삭제**
   - `.git` 폴더는 **절대 삭제 금지** (숨김 파일)
   - `README.md`는 남겨도 됨 (나중에 덮어쓰기)

---

### STEP 3: 새 파일 복사

1. **Solar Guide 프로젝트 폴더**에서 아래 파일·폴더를 **모두 선택**:
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
   ✅ css/ (폴더 전체)
   ✅ js/ (폴더 전체)
   ✅ README.md
   ✅ DEPLOYMENT_GUIDE.md
   ✅ GOOGLE_ANALYTICS_GUIDE.md
   ```

2. **복사** → 클론한 레포지토리 폴더에 **붙여넣기**

---

### STEP 4: 변경사항 커밋 및 푸시

1. **GitHub Desktop**으로 돌아가기
2. 왼쪽 패널에서 **변경된 파일 목록** 확인
3. 왼쪽 하단 입력창에 커밋 메시지 작성:
   ```
   솔라가이드 웹사이트 배포
   ```
4. **Commit to main** 버튼 클릭
5. 상단의 **Push origin** 버튼 클릭 (GitHub에 업로드)

---

### STEP 5: Netlify 자동 배포 확인

1. **1~3분 대기** (GitHub → Netlify 자동 연동)
2. https://solguide.net 접속하여 확인

---

## ✅ 배포 확인 체크리스트

- [ ] https://solguide.net → 메인 페이지 정상 로드
- [ ] 네비게이션 메뉴 9개 모두 작동
- [ ] 수익 계산기(/calculator.html) 입력·결과 표시
- [ ] 비즈니스 모델 페이지(/business.html) 블로그 링크
- [ ] 모바일 반응형 확인
- [ ] 파비콘(favicon.svg) 표시

---

## 🔧 문제 해결

### Q1: GitHub Desktop에 레포지토리가 안 보여요
→ GitHub 웹사이트에서 레포지토리 URL 복사 → GitHub Desktop **File** → **Clone repository** → **URL** 탭에 붙여넣기

### Q2: Push가 안 돼요 (권한 오류)
→ GitHub Desktop에서 **File** → **Options** → **Accounts** → 계정 재로그인

### Q3: Netlify에 자동 배포가 안 돼요
→ Netlify 대시보드 → 사이트 → **Site settings** → **Build & deploy** → **Link repository** 확인

### Q4: 배포 후에도 기존 사이트가 보여요
→ 브라우저 캐시 삭제 (`Ctrl + Shift + R`)  
→ 시크릿 모드로 확인  
→ Netlify **Deploys** 탭에서 최신 배포 상태 확인

---

## 🎉 성공 후 작업

1. ✅ **Google Analytics 설치** (GOOGLE_ANALYTICS_GUIDE.md 참고)
2. ✅ **네이버 블로그 포스팅**: "솔라가이드 웹사이트 오픈!"
3. ✅ **Google Search Console & 네이버 웹마스터** 등록
4. ✅ **SNS 공유** (페이스북, 카카오톡 등)

---

## 📞 추가 지원

- GitHub Desktop 가이드: https://docs.github.com/en/desktop
- Netlify 문서: https://docs.netlify.com/
- 문제 발생 시: 에러 메시지 스크린샷 공유

---

**작성일**: 2026-02-14  
**버전**: 1.0
