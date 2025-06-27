# 모바일 Jekyll 블로깅 시스템 설계

## 1. 현재 상황 분석

### Jekyll 블로그 특성
- 정적 사이트 생성기
- GitHub Pages 호스팅
- 마크다운 포스트 (`_posts/` 폴더)
- 이미지는 `/images/` 폴더에 저장
- 컨테이너 최대 너비: 700px

### 모바일 블로깅의 제약사항
- Jekyll은 데스크톱 환경에서 주로 사용
- 이미지 업로드 및 최적화 필요
- Git 기반 워크플로우

## 2. 기본 모바일 블로깅 방법들

### A. GitHub 웹 인터페이스
- **장점**: 가장 직접적, 별도 설정 불필요
- **단점**: 이미지 업로드가 번거로움
- **과정**: 
  1. GitHub 모바일 앱에서 `images/` 폴더에 이미지 업로드
  2. `_posts/` 폴더에 마크다운 파일 생성
  3. 이미지 참조: `![alt text](/images/filename.jpg)`

### B. 맥미니 + SSH 접근
- **환경**: 집의 맥미니에 Jekyll 환경 구성
- **접근**: Terminus 등 SSH 클라이언트로 원격 접속
- **도구**: Claude Code 활용하여 포스트 생성

## 3. 이미지 최적화 시스템

### 현재 블로그 레이아웃 기준 최적 크기
- 컨테이너 최대 너비: 700px
- 이미지 최대 너비: 95% (665px)
- **권장 크기**: 800px (레티나 디스플레이 대응)

### 자동 이미지 최적화 스크립트
```bash
#!/bin/bash
# iCloud 동기화 폴더 모니터링
fswatch ~/Library/Mobile\ Documents/com~apple~CloudDocs/blog-images | while read file; do
  if [[ "$file" =~ \.(jpg|jpeg|png)$ ]]; then
    # 자동 방향 보정 + 리사이징 + 품질 최적화
    magick "$file" -auto-orient -resize 800x800\> -strip -quality 85 \
      ~/jekyll-site/images/$(basename "$file")
    echo "Optimized: $(basename "$file")"
  fi
done
```

### 이미지 업로드 플로우
1. 모바일에서 iCloud/Dropbox에 사진 업로드
2. 맥미니에서 자동 동기화
3. 자동 최적화 스크립트로 Jekyll images/ 폴더로 이동
4. Claude Code가 포스트에서 이미지 참조

## 4. 전용 모바일 앱 개발

### 기술 스택 비교

| 구분 | React Native | Swift/SwiftUI |
|------|-------------|---------------|
| **구현 난이도** | ⭐⭐ (웹 기술 활용) | ⭐⭐⭐⭐ (Swift 학습 필요) |
| **AI 통합** | ⭐⭐⭐⭐⭐ (JavaScript API 호출) | ⭐⭐⭐ (네이티브 구현 복잡) |
| **테스트** | ⭐⭐⭐⭐ (Jest, 친숙함) | ⭐⭐⭐ (XCTest 학습 필요) |
| **성능** | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| **크로스 플랫폼** | ⭐⭐⭐⭐⭐ | ⭐ (iOS 전용) |

**추천**: React Native + Expo

### 앱 주요 기능
- 📝 마크다운 에디터 (실시간 프리뷰)
- 📷 사진 촬영/선택 → 자동 최적화 (800px)
- 🔄 GitHub API 연동으로 직접 커밋
- 📱 오프라인 임시저장
- 🎨 포스트 템플릿

## 5. 개인 지식 허브 통합 아키텍처

### 전체 시스템 구조
```
개인 서버 (맥미니)
├── Knowledge Base (Obsidian/SQLite)
├── REST API Server (Express/FastAPI)
├── Content Processing Pipeline
└── Jekyll Integration

모바일 앱
├── 주제 입력
├── 지식 베이스 검색
├── Claude API 호출 (개요 생성)
├── 초안 작성
└── Jekyll 포스트 변환
```

### 컨텐츠 생성 플로우
```
1. 모바일에서 주제 입력
2. 개인 API로 지식 베이스 검색
3. Claude API로 개요 생성
4. 사용자 피드백 반영
5. Claude API로 초안 작성
6. 이미지 최적화 및 첨부
7. Jekyll 포스트 형식으로 변환
8. Git 커밋 및 배포
```

### API 설계 예시
```javascript
// 개인 서버 API
GET  /api/knowledge/search?q=topic
POST /api/content/outline
POST /api/content/draft
POST /api/images/optimize
POST /api/jekyll/publish
```

## 6. 구현 우선순위

### Phase 1: 기본 모바일 블로깅
1. 맥미니 Jekyll 환경 구성
2. iCloud 이미지 동기화 설정
3. 자동 최적화 스크립트 구현
4. SSH + Claude Code 워크플로우 확립

### Phase 2: 전용 앱 개발
1. React Native + Expo 기본 앱 생성
2. 마크다운 에디터 구현
3. 이미지 처리 기능
4. GitHub API 연동

### Phase 3: AI 통합
1. 개인 지식 베이스 구축
2. REST API 서버 개발
3. Claude API 통합
4. 자동 컨텐츠 생성 파이프라인

## 7. 예상 효과

- **편의성**: 모바일에서 언제든 블로그 포스팅
- **품질**: AI 기반 컨텐츠 생성으로 일관된 품질
- **효율성**: 개인 지식 베이스 활용으로 시간 단축
- **일관성**: 자동화된 이미지 최적화 및 포맷팅