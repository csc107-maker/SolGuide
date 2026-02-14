# 🔄 solguide.net 파일 교체 가이드

## 📋 현재 상황
- **도메인**: solguide.net ✅
- **현재 사이트**: Tanstack Chat
- **목표**: 솔라가이드(태양광 웹사이트)로 교체

---

## 🎯 호스팅 플랫폼별 교체 방법

### 1️⃣ Netlify인 경우 (가능성 높음)

#### STEP 1: Netlify 로그인
```
https://app.netlify.com/
```
- Tanstack Chat을 배포했던 계정으로 로그인

#### STEP 2: 현재 사이트 찾기
- 대시보드에서 solguide.net 연결된 사이트 찾기
- 사이트 이름 클릭

#### STEP 3: 새 배포 업로드
1. **"Deploys"** 탭 클릭
2. 화면 중앙의 **"Drag and drop"** 영역에
3. **프로젝트 폴더 전체**를 드래그 앤 드롭

**업로드할 파일 목록:**
```
solar-guide/
├── index.html
├── calculator.html
├── finance.html
├── business.html
├── contractors.html
├── equipment.html
├── diy.html
├── investment.html
├── favicon.svg
├── css/
│   ├── style.css
│   └── calculator.css
└── js/
    ├── main.js
    └── calculator.js
```

#### STEP 4: 배포 완료 대기
- 업로드 진행 (1-2분)
- "Published" 상태 확인

#### STEP 5: 확인
```
https://solguide.net 접속
→ 솔라가이드 홈페이지 확인!
```

---

### 2️⃣ Vercel인 경우

#### STEP 1: Vercel 로그인
```
https://vercel.com/
```

#### STEP 2: 프로젝트 찾기
- Dashboard에서 solguide.net 프로젝트

#### STEP 3: 재배포
1. 프로젝트 클릭
2. **"Deployments"** 탭
3. 파일 업로드 또는 GitHub 저장소 연결

---

### 3️⃣ 일반 웹호스팅 (FTP)

#### STEP 1: FTP 클라이언트 다운로드

**FileZilla (무료):**
```
https://filezilla-project.org/
→ Download FileZilla Client
→ 설치
```

#### STEP 2: FTP 정보 확인

호스팅 업체에서 받은 정보:
```
FTP 주소: ftp.solguide.net (또는 IP 주소)
FTP 아이디: _____________
FTP 비밀번호: _____________
포트: 21 (기본값)
```

💡 **정보 찾는 방법:**
- 호스팅 업체 이메일 확인
- 호스팅 관리 페이지 로그인
- 고객센터 문의

#### STEP 3: FileZilla 접속

1. **FileZilla 실행**
2. 상단 입력란에 정보 입력:
   ```
   호스트: ftp.solguide.net
   사용자명: FTP 아이디
   비밀번호: FTP 비밀번호
   포트: 21
   ```
3. **"빠른 연결"** 클릭

#### STEP 4: 기존 파일 백업 (중요!)

**오른쪽 창 (서버):**
1. `public_html` 또는 `www` 폴더 열기
2. 모든 파일 선택
3. 로컬에 다운로드 (백업)

#### STEP 5: 기존 파일 삭제

- 서버의 모든 파일 선택 → 삭제
- ⚠️ 백업 완료 후에만 삭제!

#### STEP 6: 새 파일 업로드

**왼쪽 창 (로컬):**
- 프로젝트 폴더로 이동

**모든 파일 선택:**
```
index.html
calculator.html
finance.html
business.html
contractors.html
equipment.html
diy.html
investment.html
favicon.svg
css 폴더
js 폴더
```

**오른쪽 창 (서버)으로 드래그**
- 업로드 진행 대기 (5-10분)

#### STEP 7: 권한 설정 (필요 시)

HTML 파일 우클릭 → **"파일 속성"**
- 권한: `644` 또는 `755`

#### STEP 8: 확인
```
https://solguide.net 접속
→ 솔라가이드 확인!
```

---

## 🔍 호스팅 플랫폼 확인 방법

### 방법 1: 브라우저 개발자 도구

```
1. https://solguide.net 접속
2. F12 키 누르기
3. "Network" 탭 클릭
4. 페이지 새로고침 (F5)
5. 첫 번째 요청 클릭
6. "Response Headers" 확인
```

**결과 예시:**
```
server: Netlify         → Netlify 호스팅
x-vercel-id: ...        → Vercel 호스팅
server: Apache          → 일반 웹호스팅
server: nginx           → 일반 웹호스팅
```

### 방법 2: DNS 조회

```
https://mxtoolbox.com/SuperTool.aspx

입력: solguide.net
→ A Record 확인
```

**결과 예시:**
```
75.2.60.5           → Netlify
76.76.21.21         → Vercel
기타 IP             → 일반 호스팅
```

---

## ⚡ 빠른 해결 (추천)

### 🎯 Netlify일 가능성이 높습니다

왜냐하면:
- ✅ Tanstack는 주로 Netlify에서 호스팅
- ✅ 도메인 연결이 이미 완료됨
- ✅ 배포가 매우 간단

**지금 바로 해보세요:**

1. ✅ https://app.netlify.com/ 로그인
2. ✅ 사이트 목록에서 solguide.net 찾기
3. ✅ "Deploys" → 프로젝트 폴더 드래그
4. ✅ 2분 대기
5. ✅ https://solguide.net 확인!

---

## 📞 추가 도움

### 호스팅 플랫폼을 모르겠다면?

**확인해주세요:**

1. **이메일 검색**
   - "solguide.net" 키워드로 이메일 검색
   - 호스팅/배포 관련 이메일 확인

2. **브라우저 북마크**
   - Netlify/Vercel/GitHub 북마크 확인

3. **결제 내역**
   - 카드 결제 내역에서 호스팅 업체 확인

### 정보를 알려주시면

다음 정보를 주시면 정확한 가이드 드립니다:
- [ ] 호스팅 플랫폼 (Netlify/Vercel/기타)
- [ ] FTP 정보 유무
- [ ] 기존 배포 방법

---

## ✅ 체크리스트

### 배포 전
- [ ] 프로젝트 파일 준비 완료
- [ ] 기존 사이트 백업 (FTP인 경우)
- [ ] 호스팅 플랫폼 확인

### 배포 중
- [ ] 파일 업로드 완료
- [ ] 에러 없이 배포 완료
- [ ] 빌드 성공 확인

### 배포 후
- [ ] https://solguide.net 접속 확인
- [ ] 모든 페이지 작동 확인
- [ ] 계산기 기능 테스트
- [ ] 모바일 확인
- [ ] 블로그 링크 확인

---

## 🎉 배포 완료 후

1. ✅ Google Analytics 설치
2. ✅ 블로그에 새 URL 공유
3. ✅ SNS 홍보 시작

---

**다음 정보를 알려주시면 정확한 방법으로 안내해드리겠습니다:**

1. Netlify/Vercel/GitHub 중 어떤 것을 사용하시나요?
2. FTP 정보를 가지고 계신가요?
3. 기존에 어떻게 Tanstack Chat을 배포하셨나요?

바로 도와드리겠습니다! 😊
