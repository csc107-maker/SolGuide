# Netlify CLI로 Solar Guide 배포하기

## 📦 준비 사항
- Node.js 설치 필요 (https://nodejs.org/)
- 프로젝트 폴더 준비

---

## 🚀 배포 단계

### STEP 1: Netlify CLI 설치
터미널(명령 프롬프트) 열고:
```bash
npm install -g netlify-cli
```

### STEP 2: Netlify 로그인
```bash
netlify login
```
→ 브라우저가 열리면 **Authorize** 클릭

### STEP 3: 프로젝트 폴더로 이동
```bash
cd C:\경로\solguide-project
```

### STEP 4: 배포
```bash
netlify deploy --prod
```

→ **"Publish directory"** 질문에 `.` (현재 폴더) 입력  
→ 배포 완료 후 URL 확인

---

## ✅ 성공 확인
- Website Draft URL: https://solguide.net
- Logs: Netlify 대시보드에서 확인

---

## 🔧 문제 해결

### Q: `npm: command not found`
→ Node.js 설치: https://nodejs.org/

### Q: 권한 오류
→ 관리자 권한으로 실행 (Windows: 명령 프롬프트 우클릭 → 관리자 권한)

### Q: 잘못된 폴더에 배포됨
→ `cd` 명령으로 정확한 폴더 위치 확인

---

**작성일**: 2026-02-14
