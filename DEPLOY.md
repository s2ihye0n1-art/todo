# GitHub Pages 배포 가이드

## 🚀 자동 배포 (GitHub Actions)

### 설정 방법

1. **GitHub 저장소 설정**
   - GitHub 저장소 → Settings 클릭
   - Pages 섹션으로 이동
   - Source: GitHub Actions 선택

2. **배포 (자동)**
   - 이 저장소에 commit & push하면 자동으로 배포됩니다!
   - `.github/workflows/deploy.yml`이 자동으로 실행됩니다

3. **배포 상태 확인**
   - Actions 탭에서 "Deploy to GitHub Pages" 워크플로우 확인
   - 초록색 체크 마크 = 배포 완료! ✅

### 배포된 웹사이트

```
https://s2ihye0n1-art.github.io/todo/
```

---

## 📝 수동 배포 (선택사항)

만약 자동 배포가 작동하지 않으면, CMD에서:

```cmd
cd %USERPROFILE%\todo
npm run build
npm run deploy
```

---

## ✅ 배포 확인

1. https://s2ihye0n1-art.github.io/todo/ 접속
2. Mindful Todo 앱이 보이면 성공! 🎉
3. 할 일을 추가해보세요!
4. 페이지 새로고침해도 데이터가 유지됩니다 (localStorage)

---

## 🔧 문제 해결

### "404 Page not found" 오류

`vite.config.ts`에 `base: '/todo/'`가 설정되어 있는지 확인하세요.

### 변경사항이 적용되지 않음

- GitHub Actions 워크플로우가 완료될 때까지 기다리세요 (2-3분)
- 브라우저 캐시 삭제: Ctrl + Shift + Delete

### 로컬 스토리지 데이터가 초기화됨

GitHub Pages 배포 후 처음 접속하면 데이터가 새로 생성됩니다.
(각 환경에서 독립적으로 localStorage 관리)

---

## 📊 배포 워크플로우

```
1. Commit & Push to main
   ↓
2. GitHub Actions 자동 실행
   ↓
3. npm install & npm run build
   ↓
4. dist 폴더 생성
   ↓
5. GitHub Pages에 배포
   ↓
6. https://s2ihye0n1-art.github.io/todo/ 업데이트 ✅
```

---

## 💡 팁

- 로컬에서 테스트: `npm run dev`
- 프로덕션 빌드: `npm run build`
- 배포: 자동으로 진행됨!
- 상태 확인: GitHub Actions 탭

---

**이제 준비가 완료되었습니다!** 🚀
아무것도 할 필요 없이 commit & push하면 자동으로 배포됩니다!
