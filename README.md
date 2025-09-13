![MIT License](https://img.shields.io/badge/license-MIT-green)
![GitHub Actions](https://github.com/jeeqong/jq-sitemap-for-tistory/actions/workflows/deploy.yml/badge.svg)

# jq-sitemap-for-tistory 🛰️

**티스토리 블로그**를 위한 자동 사이트맵 생성기입니다.  
블로그 글 목록을 크롤링하여 `sitemap.xml` 파일을 자동으로 만들어줍니다.
검색엔진 색인 최적화를 위해 sitemap.xml을 직접 생성해 업로드할 수 있습니다.

## 🔥 주요 기능

- 티스토리 글 목록을 크롤링하여 `sitemap.xml` 자동 생성
- /category 의 글목록을 크롤링함
- 날짜 기반 정렬 및 중복 제거
- 매일 am 3:00 자동 갱신

🔗 [Introduce](https://jeeqong.tistory.com/entry/tistory-sitemap-generator-intro-jq-sitemap)

---

## 설정

### 📦 사용 방법

1. 깃허브 계정 추가
2. https://github.com/jeeqong/jq-sitemap-for-tistory 접속후 Fork
3. Github Action 활성화
4. config.json 수정
5. GitHub Pages 활성화
6. sitemap.xml 확인

🔗 [설정가이드](https://jeeqong.tistory.com/entry/tistory-sitemap-generator-guide)

### ⚙️ config.json 예시

```
{
  "blog_url": "https://jeeqong.tistory.com",   // 블로그 주소
  "max_pages": 10 // 리스트 페이지 갯수
}
```

### ✅ 적용 가능한 Tistory 스킨 목록 (2025.04 기준)

| **스킨 이름** | **지원 여부** | **비고**                       |
| ------------- | ------------- | ------------------------------ |
| BookClub      | ✅ 사용 가능  | 안정적 구조                    |
| Ray           | ✅ 사용 가능  |                                |
| Ray2          | ✅ 사용 가능  |                                |
| xf_Letter     | ✅ 사용 가능  |                                |
| xf_Magazine   | ✅ 사용 가능  |                                |
| xf_Odyssey    | ✅ 사용 가능  |                                |
| xf_Portfolio  | ✅ 사용 가능  |                                |
| xf_Poster     | 🔺 부분 가능  | **날짜 데이터 없음**           |
| Square        | ❌ 사용 불가  | **모든 요소가 구분 불가 구조** |

#### 🛠️ 참고사항

- ❌ 제외된 스킨은 sitemap.xml 생성 시 게시글 날짜 추출이 불가능하거나, <a> 태그가 인기글/연관글과 구분되지 않아 자동화 불가한 구조입니다.
- ✅ 스킨들은 정규 표현식 기반으로 날짜와 링크 추출이 검증되었습니다.
- 스킨에 따라 class명 없이 구조만으로 분석하는 경우가 많아 스킨 구조 변경 시 다시 확인이 필요합니다.
- `🔺 xf_Poster` 스킨은 해당스킨에 날짜가 지원되지 않아 url 만 생성합니다.

---

### 🪪 라이선스

MIT License.
`JQ SiteMap`은 이 MIT 라이선스를 따릅니다.

- 누구나 자유롭게 사용, 수정, 배포할 수 있어요.
- 상업적 이용도 가능합니다.

📌 단, 꼭 지켜야 할 조건

- 저작자(제작자) 정보를 삭제하거나 숨기면 안 됩니다.
- LICENSE 파일에 포함된 원작자 정보와 저작권 고지는 유지해야 합니다.
- 프로젝트는 “있는 그대로(as-is)” 제공되며, 문제 발생 시 제작자는 책임지지 않습니다.

---

> Created with ❤️ by [jeeqong](https://jeeqong.tistory.com)
