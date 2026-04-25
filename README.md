# 100일 나침반 진단

습관화 프로젝트 3기 참가자를 위한 적응형 웹 진단 도구.
밥 프록터의 C형 목표(간절하지만 방법을 모르는 것)를 찾는 데 초점.

## 구조

- 단일 `index.html` 파일 (Chart.js · html2canvas · Pretendard CDN)
- LocalStorage 기반 진행 상태 저장 (Phase 간 이동 허용)
- 100% 선택형 · 모바일 우선 (최대 너비 640px)
- 8축 갈망 프로필 · 적응형 토너먼트 · 인사이트 브레이크

## 진행 단계

| Phase | 문항 | 시간 | 인사이트 브레이크 |
|---|---|---|---|
| Phase 1 — 제약 해제 + 순수 갈망 | 48 | 25~30분 | 3회 |
| Phase 2 — C형 목표 형성 + 간절함 검증 | 47 | 30~35분 | 3회 |
| Phase 3 — 100일 중간 목표 + 현재 상태 | 23 | 18~22분 | 2회 |
| **합계** | **118** | **73~87분** | **8회** |

현재 구현 범위: **Phase 1 전체 + 인사이트 브레이크 #1~#3**.

## 로컬 실행

```bash
python3 -m http.server 8765
# http://localhost:8765 접속
```

CDN을 쓰기 때문에 파일 더블클릭(`file://`)이 아닌 HTTP 서빙을 권장합니다.

## 배포

Netlify 정적 호스팅:

```bash
npm install -g netlify-cli
netlify deploy --prod --dir=.
```

## 디자인 시스템

- 색상: 네이비 `#1B2A4A` + 틸 `#1A8F6A`
- 폰트: Pretendard Variable
- 카드 라운드 16px, 버튼 라운드 12px, 카드 그림자 `0 2px 12px rgba(27,42,74,.06)`

## 분석

Google Analytics: `G-KJNV6DHSGC`

발화 이벤트: `compass_start`, `compass_ib`, `compass_phase_complete`, `compass_save_result`.

---

© BRIDGE Team
