# Subjective Experience Shopping Platform

리뷰에 담긴 사용 경험을 상품 검색과 비교에 활용하는 카탈로그 프로젝트입니다.

이 저장소는 조직 소개와 프로젝트 안내를 관리합니다. GitHub 조직 첫 화면의 소개는 [profile/README.md](profile/README.md)에서 확인할 수 있습니다.

## 저장소

| 저장소 | 역할 |
| --- | --- |
| [semantic-review-extraction-experiment](https://github.com/subjective-experience-shopping-platform/semantic-review-extraction-experiment) | 리뷰 속성 추출과 정규화 방식의 2×2 실험 및 평가 |
| [review-catalog-platform](https://github.com/subjective-experience-shopping-platform/review-catalog-platform) | 신규 리뷰 처리, 카탈로그 버전 관리, 보고서 생성과 재군집화 |
| [meta-search](https://github.com/subjective-experience-shopping-platform/meta-search) | 객관·체감·판매 속성을 통합하여 검색하고 비교하는 MCP 서버 |
| [review-catalog-platform-demo](https://github.com/subjective-experience-shopping-platform/review-catalog-platform-demo) | 모니터 9개를 대상으로 검색·대화·리뷰 분석을 제공하는 웹 데모 |

## 운영

- [웹 데모](https://subjective-experience-shopping-platform.github.io/review-catalog-platform-demo/#chat)는 GitHub Pages와 AWS Lambda를 사용합니다.
- `review-catalog-platform`은 로컬 실행과 CI 검증을 기본으로 합니다. AWS 배포 코드는 보존하지만 새 조직에서 활성화하지 않습니다.
- API 키, 인증 토큰, 모델 가중치와 운영 로그는 공개 저장소에 포함하지 않습니다.

## 라이선스

조직의 프로젝트 코드는 [GNU GPL 3.0](LICENSE)을 따릅니다. 외부 데이터셋과 모델의 이용 조건은 각 원본 제공처의 조건을 따릅니다.
