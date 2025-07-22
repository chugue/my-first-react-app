# 🎬 영화 검색 웹 애플리케이션

## 📋 프로젝트 개요
TMDB API를 활용한 실시간 영화 검색 및 인기 영화 추천 서비스입니다. 사용자의 검색 패턴을 분석하여 트렌딩 영화를 제공하는 반응형 웹 애플리케이션입니다.

## 🚀 주요 기능
- **실시간 영화 검색**: Debounce를 적용한 효율적인 검색 기능
- **트렌딩 영화 표시**: 사용자들의 검색 빈도를 기반으로 한 인기 영화 추천
- **영화 정보 표시**: 평점, 개봉일, 언어 등 상세 정보 제공
- **반응형 디자인**: 모바일부터 데스크톱까지 모든 디바이스 지원

## 🛠 기술 스택

### Frontend
- **React 19.1.0** - 최신 버전의 React를 활용한 컴포넌트 기반 UI 개발
- **Tailwind CSS 4.1.11** - 유틸리티 퍼스트 CSS 프레임워크로 빠른 스타일링
- **Vite 7.0.4** - 빠른 개발 환경 및 최적화된 빌드 시스템

### Backend & Database
- **Appwrite 18.1.1** - BaaS(Backend as a Service)를 활용한 데이터베이스 관리
  - 검색어 저장 및 카운팅
  - 트렌딩 데이터 관리

### External API
- **TMDB API** - 영화 데이터 및 이미지 제공

### 개발 도구
- **ESLint** - 코드 품질 관리
- **React Hooks** - 함수형 컴포넌트와 상태 관리
- **react-use** - useDebounce를 활용한 검색 최적화

## 📁 프로젝트 구조
```
my-first-react-app/
├── src/
│   ├── components/
│   │   ├── MovieCard.jsx      # 영화 카드 컴포넌트
│   │   ├── Search.jsx         # 검색 입력 컴포넌트
│   │   └── Spinner.jsx        # 로딩 스피너 컴포넌트
│   ├── App.jsx                # 메인 애플리케이션 컴포넌트
│   ├── appwrite.js            # Appwrite 데이터베이스 연동
│   ├── App.css                # 애플리케이션 스타일
│   └── main.jsx               # 애플리케이션 진입점
├── public/                    # 정적 리소스
├── vite.config.js            # Vite 설정
└── package.json              # 프로젝트 의존성
```

## 💡 주요 구현 사항

### 1. 검색 최적화
- `useDebounce` 훅을 활용하여 500ms 디바운싱 적용
- 불필요한 API 호출 최소화로 성능 향상

### 2. 상태 관리
- React Hooks (useState, useEffect)를 활용한 효율적인 상태 관리
- 로딩 상태, 에러 처리 구현

### 3. 데이터베이스 연동
- Appwrite를 활용한 검색어 저장 및 통계 관리
- 실시간 트렌딩 데이터 업데이트

### 4. UI/UX
- Tailwind CSS를 활용한 반응형 디자인
- 스켈레톤 로딩 및 에러 메시지 표시
- 영화 포스터 이미지 최적화

## 🔧 설치 및 실행

### 환경 변수 설정
`.env` 파일 생성 후 다음 변수 설정:
```
VITE_TMDB_API_KEY=your_tmdb_api_key
VITE_APPWRITE_ENDPOINT=your_appwrite_endpoint
VITE_APPWRITE_PROJECT_ID=your_project_id
VITE_APPWRITE_DATABASE_ID=your_database_id
VITE_APPWRITE_COLLECTION_ID=your_collection_id
```

### 설치 및 실행
```bash
# 의존성 설치
npm install

# 개발 서버 실행
npm run dev

# 프로덕션 빌드
npm run build

# 빌드 미리보기
npm run preview
```

## 🌐 배포
- Vercel을 통한 자동 배포 구성
- `vercel.json` 설정 파일 포함

## 📈 성과 및 학습
- **React 최신 버전** 활용 경험
- **BaaS 서비스** 통합 및 활용
- **외부 API** 연동 및 에러 핸들링
- **성능 최적화** 기법 (Debouncing, 이미지 최적화)
- **반응형 웹 디자인** 구현

---

### 🔗 관련 링크
- [TMDB API Documentation](https://www.themoviedb.org/documentation/api)
- [Appwrite Documentation](https://appwrite.io/docs)
- [Tailwind CSS](https://tailwindcss.com/)