# Google Analytics 설정 가이드

## 📊 Google Analytics란?

웹사이트 방문자 통계를 추적하고 분석할 수 있는 무료 도구입니다.
- 방문자 수
- 페이지뷰
- 유입 경로
- 사용자 행동 패턴

---

## 🚀 설정 방법 (단계별)

### 1단계: Google Analytics 계정 만들기

1. **Google Analytics 접속**
   - 웹사이트: https://analytics.google.com/
   - Google 계정으로 로그인

2. **"측정 시작" 클릭**

3. **계정 정보 입력**
   - 계정 이름: "솔라가이드" (원하는 이름)
   - 데이터 공유 설정: 기본값 유지
   - "다음" 클릭

---

### 2단계: 속성 만들기

1. **속성 이름**: "솔라가이드 웹사이트"
2. **보고 시간대**: 대한민국 (GMT+09:00)
3. **통화**: 대한민국 원 (KRW)
4. **"다음" 클릭**

---

### 3단계: 비즈니스 정보 입력

1. **업종**: "기타 비즈니스 또는 전문 서비스"
2. **비즈니스 규모**: 소규모 (1-10명)
3. **Google Analytics 사용 목적**:
   - ✅ 웹사이트 또는 앱의 사용자 행동 검토
   - ✅ 비즈니스 목표 측정
4. **"만들기" 클릭**

---

### 4단계: 데이터 스트림 설정

1. **플랫폼 선택**: "웹"
2. **웹사이트 URL 입력**:
   - GitHub Pages: `https://your-username.github.io/your-repo`
   - Netlify: `https://your-site.netlify.app`
   - Vercel: `https://your-site.vercel.app`
3. **스트림 이름**: "솔라가이드 메인"
4. **"스트림 만들기" 클릭**

---

### 5단계: 측정 ID 확인

설정이 완료되면 다음과 같은 형식의 ID가 표시됩니다:

```
G-XXXXXXXXXX
```

이 ID를 복사하세요! (예: G-ABC123XYZ)

---

## 💻 웹사이트에 코드 추가하기

### 방법 1: 모든 페이지에 직접 추가 (권장)

각 HTML 파일의 `<head>` 태그 안에 아래 코드를 추가하세요:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

**⚠️ 중요**: `G-XXXXXXXXXX` 부분을 실제 측정 ID로 변경하세요!

**추가할 파일 목록**:
- index.html
- calculator.html
- finance.html
- business.html
- contractors.html
- equipment.html
- diy.html
- investment.html

---

### 방법 2: 공통 JavaScript 파일에 추가

`js/analytics.js` 파일을 만들고:

```javascript
// Google Analytics
(function() {
  var script = document.createElement('script');
  script.async = true;
  script.src = 'https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX';
  document.head.appendChild(script);

  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
})();
```

그리고 모든 HTML 파일의 `</body>` 태그 직전에:

```html
<script src="js/analytics.js"></script>
```

---

## ✅ 설치 확인하기

### 1. 실시간 보고서로 확인

1. Google Analytics 대시보드로 이동
2. 왼쪽 메뉴에서 **"보고서" > "실시간"** 클릭
3. 웹사이트를 새 탭에서 열기
4. 1분 이내에 방문자가 표시되면 성공!

### 2. 브라우저 개발자 도구로 확인

1. 웹사이트를 Chrome에서 열기
2. `F12` 키 누르기
3. "Network" 탭 클릭
4. 페이지 새로고침
5. "gtag" 또는 "analytics" 검색
6. 요청이 보이면 정상 작동 중!

---

## 📊 유용한 보고서

### 1. 획득 보고서
- 방문자가 어디서 왔는지 확인
- 검색엔진, 소셜미디어, 직접 방문 등

### 2. 참여도 보고서
- 어떤 페이지가 가장 인기있는지
- 평균 체류 시간

### 3. 전환 보고서
- 목표 달성 추적 (상담 신청, 계산기 사용 등)

---

## 🎯 목표(Goal) 설정하기

특정 행동을 추적하려면 목표를 설정하세요:

### 예시 1: 상담 신청 완료
1. **관리** > **이벤트** > **이벤트 만들기**
2. 이벤트 이름: `contact_submit`
3. 조건: 페이지 URL에 `#contact` 포함

### 예시 2: 계산기 사용
1. 이벤트 이름: `calculator_use`
2. 조건: 페이지 URL이 `calculator.html`

---

## 🔒 개인정보 보호

### GDPR/개인정보처리방침 준수

웹사이트에 개인정보처리방침 페이지 추가 권장:

```html
<!-- Footer에 추가 -->
<a href="privacy.html">개인정보처리방침</a>
```

**내용 예시**:
> 본 웹사이트는 Google Analytics를 사용하여 방문 통계를 수집합니다.
> 수집되는 정보는 익명화되며, 개인을 식별할 수 없습니다.

---

## 📱 추가 팁

### 1. 필터 설정
- 자신의 IP 주소 제외하여 정확한 통계 확보

### 2. 이메일 알림 설정
- 주간/월간 리포트 자동 발송

### 3. 대시보드 맞춤화
- 자주 보는 지표를 한눈에 보기

---

## ❓ 문제 해결

### Analytics가 작동하지 않을 때

1. **측정 ID 확인**
   - `G-XXXXXXXXXX` 형식이 맞는지
   - 오타가 없는지

2. **코드 위치 확인**
   - `<head>` 태그 안에 있는지
   - 모든 페이지에 추가했는지

3. **브라우저 캐시 삭제**
   - `Ctrl + Shift + Delete`

4. **24시간 대기**
   - 데이터가 표시되기까지 시간이 걸릴 수 있음

---

## 🆘 도움이 필요하면

- [Google Analytics 고객센터](https://support.google.com/analytics)
- [YouTube 튜토리얼](https://www.youtube.com/results?search_query=google+analytics+4+tutorial+한국어)

---

**설정 완료 후 README.md에 기록하세요!**

```markdown
## 📊 Analytics 설정 완료
- Google Analytics 4 설치: ✅
- 측정 ID: G-XXXXXXXXXX
- 설치일: 2026-02-14
```
