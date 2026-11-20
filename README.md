# Moonlight English | The resource shelf

[판매 페이지](https://moonlang.com/moonlight-english/) · [독립 화면](https://devlog.moonlang.com/moonlight-english-shelf/)

## 상품 업데이트

**간편한 방법:** [상품 목록 편집 도구](https://devlog.moonlang.com/moonlight-english-shelf/manage.html)에서 상품을 선택하거나 추가 → 목록에 적용 → 검증 후 다운로드 → GitHub에 catalog.json을 올리고 커밋합니다. 편집 도구에서 입력한 값은 커밋 전까지 공개되지 않습니다.

직접 수정하는 방법:

1. [catalog.json 편집](https://github.com/Reasonofmoon/moonlight-english-shelf/edit/main/catalog.json)에서 공개 TPT 상품만 추가·수정합니다. 중단 상품은 해당 객체를 제거합니다.
2. 각 상품은 id(문자열), title, url(공식 구매 주소), cover(공개 표지 이미지 주소), rank(TPT Best Sellers 순위 숫자, 확인 불가 시 null)로 구성됩니다. 순위 중복은 허용하지 않습니다. TPT의 Most Recent 첫 상품 ID를 featured에, 확인 날짜를 updated에 YYYY-MM-DD로 입력합니다. 상품 수·검색·페이지·최신 표지·순서는 자동 계산됩니다.
3. 권장: 브랜치에서 수정하고 아래 검사를 실행한 후 main에 병합합니다. main 변경은 GitHub Pages가 자동 배포하며 [Actions](https://github.com/Reasonofmoon/moonlight-english-shelf/actions)에서 성공 여부를 확인합니다. WordPress에는 같은 URL을 연결하므로 재편집할 필요가 없습니다. 실제 판매 현황의 TPT → GitHub 수집은 자동이 아닙니다.
4. 배포 후 판매 페이지에서 최신 상품·상위 판매 상품·검색/링크를 확인하세요. 잘못된 변경은 GitHub에서 이전 catalog.json 복원 후 재배포하세요.

### 로컬 검증 (Node 18+)

    node check.mjs

공개 카탈로그, 등록일/수동 지정 최신 상품, 공개 판매순 및 표지 주소만 관리합니다. 운영자용 판매량·개인 데이터·구매 파일은 이 저장소에 넣지 마세요. 가격과 결제는 TPT에서 확인합니다.
