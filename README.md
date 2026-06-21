# Mindful Todo - 과부하 방지 플래너

투두리스트의 긍정적 효과는 유지하면서, 인지적 부하와 스트레스를 최소화하는 혁신적인 할 일 관리 앱입니다.

![Mindful Todo](https://img.shields.io/badge/version-0.1.0-blue)
![React](https://img.shields.io/badge/React-18.2-61DAFB?logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.2-3178C6?logo=typescript)

## 🎯 프로젝트 목적

일반적인 투두리스트는 과도한 할 일을 등록하게 하여 **인지적 과부하**를 유발하고, 미완성된 항목이 시각적으로 계속 쌓이면서 **자이가르닉 효과**로 인한 스트레스를 야기합니다.

**Mindful Todo**는 이러한 문제를 다음과 같이 해결합니다:

- ⏰ **가용 시간 예산제**: 물리적 한계를 명확히 하여 계획 오류 방지
- 🧠 **임시 보관함(Brain Dump)**: 당장 불가능한 일을 시야에서 제거하여 인지 부하 감소
- 📊 **시간 정확도 분석**: 예상 vs 실제 시간을 추적하여 계획 능력 향상
- ✅ **안전한 이월 시스템**: 미완료 작업을 스트레스 없이 다음 날로 이동

## ✨ 주요 기능

### 1. 가용 시간 설정 및 관리
- 수면/식사 등을 제외한 순수 가용 시간 입력
- 분 단위 정밀한 시간 관리
- 언제든지 변경 가능

### 2. 할 일 등록 및 검증
- 할 일 제목과 예상 소요 시간 입력
- **자동 초과 검증**: 가용 시간을 초과하면 등록 불가
- 임시 보관함 저장 옵션으로 유연한 관리

### 3. 임시 보관함 (Brain Dump)
- 당장 처리할 수 없는 작업을 별도 공간에 관리
- 시각적 스트레스 감소
- 필요할 때만 꺼내서 일정에 추가 가능

### 4. 작업 완료 및 시간 입력
- 완료 시 **실제 소요 시간** 입력
- 예상 시간과의 차이 시각화
- 시간 정확도 개선 추적

### 5. 실시간 대시보드
- 📈 시간 예산 사용률 (진행률)
- 📊 완료율 및 작업 통계
- 🎯 예상 vs 실제 소요 시간 비교 차트
- 🔄 시간 오차 분석

### 6. 안전한 이월 시스템
- 매일 새벽 2시에 미완료 작업 자동 이월
- X 아이콘으로 표시하여 실패감 감소
- 심리적 안정감 제공

## 🛠️ 기술 스택

- **Frontend Framework**: React 18.2
- **Language**: TypeScript 5.2
- **Build Tool**: Vite 5.0
- **State Management**: Zustand 4.4
- **Visualization**: Recharts 2.10
- **Date Handling**: date-fns 2.30
- **Styling**: CSS3

## 🚀 시작하기

### 필수 환경
- Node.js 16.0 이상
- npm 또는 yarn

### 설치 및 실행

```bash
# 1. 저장소 클론
git clone https://github.com/s2ihye0n1-art/todo.git
cd todo

# 2. 의존성 설치
npm install

# 3. 개발 서버 시작
npm run dev

# 4. 브라우저에서 접속
# http://localhost:5173
```

### 빌드

```bash
# 프로덕션 빌드
npm run build

# 빌드 결과 미리보기
npm run preview
```

## 📁 프로젝트 구조

```
todo/
├── src/
│   ├── components/          # React 컴포넌트
│   │   ├── Header.tsx
│   │   ├── Footer.tsx
│   │   ├── TimeBudgetSection.tsx
│   │   ├── TodoForm.tsx
│   │   ├── TodoList.tsx
│   │   ├── DailyDashboard.tsx
│   │   └── BrainDump.tsx
│   ├── store/
│   │   └── todoStore.ts     # Zustand 상태 관리
│   ├── types/
│   │   └── index.ts         # TypeScript 타입 정의
│   ├── styles/
│   │   ├── index.css        # 전역 스타일
│   │   ├── Header.css
│   │   ├── TodoForm.css
│   │   ├── TodoList.css
│   │   ├── DailyDashboard.css
│   │   └── ...
│   ├── App.tsx              # 메인 App 컴포넌트
│   └── main.tsx             # 엔트리 포인트
├── index.html
├── vite.config.ts
├── tsconfig.json
└── package.json
```

## 📋 사용 방법

### 1단계: 가용 시간 설정
1. "오늘의 가용 시간" 카드에서 "변경" 버튼 클릭
2. 순수 가용 시간 입력 (예: 360분 = 6시간)
3. 저장

### 2단계: 할 일 추가
1. "새로운 할 일 추가" 폼에 제목과 예상 시간 입력
2. "오늘 일정에 추가" 또는 "임시 보관함에 저장" 선택
3. 시간 초과 시 자동으로 경고 메시지 표시

### 3단계: 작업 추적
1. 작업 완료 시 ✓ 버튼 클릭
2. 실제 소요 시간 입력
3. 예상 시간과의 차이 자동 계산

### 4단계: 데이터 분석
1. 대시보드에서 통계 및 차트 확인
2. 시간 정확도 개선 추적
3. 다음 계획에 반영

## 🧠 핵심 개념

### 자이가르닉 효과 (Zeigarnik Effect)
완결되지 않은 과제가 뇌에 강한 잔상으로 남아 스트레스를 유발하는 심리 현상입니다.

**Mindful Todo의 해결책**:
- 임시 보관함으로 불명확한 작업 분리
- 미완료 작업의 안전한 이월로 심리적 안정

### 시간 예산제 (Time Budgeting)
정해진 시간 내에서만 작업을 계획하도록 제한합니다.

**Mindful Todo의 구현**:
- 가용 시간 설정 후 초과 불가
- 버퍼 가중치를 통한 과거 오차율 반영 (향후 업데이트 예정)

## 📊 데이터 저장

모든 데이터는 **localStorage**에 자동으로 저장됩니다.
- 브라우저 새로고침해도 데이터 유지
- 다른 탭/창에서도 실시간 동기화 가능

## 🎨 UI/UX 특징

- **직관적 디자인**: 복잡한 기능을 간단하게 표현
- **시각적 피드백**: 색상과 아이콘을 통한 상태 전달
- **반응형 디자인**: 모바일, 태블릿, 데스크톱 모두 대응
- **다크모드 준비**: CSS 변수를 통한 테마 확장 가능

## 🔮 향후 계획

- [ ] 과거 오차율 기반 버퍼(Buffer) 가중치 자동 계산
- [ ] 주간/월간 통계 분석
- [ ] 사용자 커스텀 카테고리
- [ ] 협업 기능 (공유 및 팀 작업)
- [ ] 다크 모드
- [ ] 알림 기능 (데스크톱 notification)
- [ ] 모바일 앱 (React Native)
- [ ] 클라우드 동기화 (로그인 기능)
- [ ] AI 기반 시간 예측

## 🐛 버그 리포팅 및 기능 요청

이슈가 발견되면 [GitHub Issues](https://github.com/s2ihye0n1-art/todo/issues)에서 보고해주세요.

## 📄 라이선스

이 프로젝트는 MIT 라이선스 하에 있습니다. [LICENSE](LICENSE) 파일을 참조하세요.

## 👤 작성자

- **박시현** (2026130903)
- GitHub: [@s2ihye0n1-art](https://github.com/s2ihye0n1-art)

## 🙏 감사의 말

이 프로젝트는 심리학의 자이가르닉 효과와 시간 관리의 현실적 어려움에서 영감을 받아 만들어졌습니다.

---

**스트레스 없는 생산성, Mindful Todo와 함께 시작하세요! 🌟**
