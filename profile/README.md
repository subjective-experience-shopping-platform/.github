# 리뷰의 사용 경험을 비교·검색 가능한 카탈로그로

상품의 크기와 무게, 해상도 같은 사양만으로는 실제 사용감을 충분히 설명하기 어렵습니다. 이 프로젝트는 리뷰에 담긴 사용 경험과 평가를 근거와 함께 구조화하여, 상품을 비교하고 선택하는 데 활용하고자 합니다.

리뷰에서 표현을 자유롭게 추출하면 비슷한 의미가 여러 이름으로 나뉘고, 미리 정한 속성만 사용하면 새로운 경험을 담기 어렵습니다. 이를 속성 추출과 정규화에 대한 실험으로 검토하고, 카탈로그 파이프라인과 검색 도구, 웹 데모로 연결했습니다.

**[웹 데모 사용하기](https://subjective-experience-shopping-platform.github.io/review-catalog-platform-demo/#chat)**

## 프로젝트 구성

| 프로젝트 | 다루는 문제 |
| --- | --- |
| [semantic-review-extraction-experiment](https://github.com/subjective-experience-shopping-platform/semantic-review-extraction-experiment) | 단순 속성 추출과 Opinion Units, 정규화 적용 여부를 조합한 2×2 실험으로 추출·정규화 방식을 비교합니다. |
| [review-catalog-platform](https://github.com/subjective-experience-shopping-platform/review-catalog-platform) | 리뷰 추출·검증·정규화, 증분 처리, 수동 재군집화와 카탈로그 발행을 관리합니다. |
| [meta-search](https://github.com/subjective-experience-shopping-platform/meta-search) | 상품의 객관 속성, 리뷰에서 얻은 체감 속성, 판매 조건을 MCP 도구로 검색하고 비교합니다. |
| [review-catalog-platform-demo](https://github.com/subjective-experience-shopping-platform/review-catalog-platform-demo) | 고정된 모니터 9개의 카탈로그를 바탕으로 조건 검색, 대화와 입력 리뷰 분석을 제공합니다. |

## 데모에서 확인할 수 있는 것

- 사양과 리뷰 통계, 판매 조건을 함께 고려한 상품 탐색
- 대화를 이어가며 원하는 조건을 추가하거나 변경하는 검색
- 입력 리뷰에서 추출한 의견과 기존 카탈로그를 비교하는 보고서

데모는 고정된 데이터 범위에서 동작합니다. 리뷰 통계는 객관적 성능을 보증하지 않으며, 조건에 맞는 상품이 없거나 판단 근거가 부족한 경우를 구분합니다. 판매 정보는 시연을 위한 더미 데이터입니다.

웹 데모는 GitHub Pages와 AWS Lambda로 운영합니다. 전체 카탈로그 파이프라인인 `review-catalog-platform`은 로컬에서 실행하고 GitHub Actions로 검증하며, 새 조직에서는 AWS에 연결하지 않습니다.

## 라이선스

프로젝트 코드는 [GNU GPL 3.0](https://github.com/subjective-experience-shopping-platform/.github/blob/main/LICENSE)을 따릅니다. 외부 데이터셋과 모델은 각 제공처의 이용 조건을 따릅니다.
