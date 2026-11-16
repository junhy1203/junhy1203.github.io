# 작은 도구들 — JunHyuk의 앱과 개발 기록

**직접 만든 앱을 소개하고 사용법을 정리한 정적 웹사이트**의 공개 배포 저장소입니다. 방문자가 앱을 찾을 수 있는 목록, 앱별 소개 글, 소개·문의·정책 페이지로 구성되어 있습니다.

[사이트 열기](https://junhyuk.site/) · [콘텐츠 생성 프로젝트](https://github.com/junhy1203/app-journal)

## 사이트 구성

- **메인:** 최신 소개 글과 프로젝트 모음
- **앱 목록:** 사용 가능한 도구를 분류해 탐색
- **사용 가이드:** Superword, PDF 도구, GeminiChat Studio 등을 소개하는 개별 페이지
- **안내:** 소개, 문의, 개인정보처리방침, 이용약관
- **검색 접근성:** 사이트맵, robots.txt, 구조화 데이터 및 개별 HTML 경로

## 이 저장소의 역할

루트의 `index.html`, `apps/`, `posts/`, `styles.css`, `app.js` 등은 **정적 사이트 배포 결과물**입니다. `journal-source/`에는 같은 유형의 콘텐츠 생성 소스가 포함되어 있으며, 별도 [app-journal](https://github.com/junhy1203/app-journal) 저장소에서도 사이트를 관리합니다.

| 경로 | 내용 |
| --- | --- |
| `index.html` | 사이트 첫 화면 |
| `apps/`, `posts/` | 앱 디렉터리 및 개별 소개 글 |
| `about/`, `contact/` | 운영자 및 연락 안내 |
| `privacy/`, `terms/` | 정책 페이지 |
| `journal-source/` | 콘텐츠·사이트 생성 스크립트 |
| `CNAME` | 사용자 정의 도메인 설정 |
| `sitemap.xml`, `robots.txt` | 검색엔진용 파일 |

## 로컬에서 미리보기

현재 배포 페이지 그대로 확인하려면 저장소 루트에서:

```bash
python -m http.server 8080
```

단, 내부 링크가 루트 절대경로이므로 `http://localhost:8080/`에서 확인해야 합니다.

사이트 생성 소스를 직접 확인하려면:

```bash
cd journal-source
npm run build
npm run check
npm run dev
```

해당 폴더의 Node.js 명령은 코드에 있는 `package.json`을 기준으로 합니다. **생성된 HTML을 직접 수정하면 이후 재빌드 시 덮어써질 수 있습니다.** 원본 콘텐츠·설정을 먼저 수정하세요.

## 운영 참고

실제 외부 사이트 주소, 공개 링크와 도메인 설정은 배포할 때 확인해야 합니다. 사이트에 소개된 제3자 서비스·라이브러리는 각 서비스의 이용 조건이 적용됩니다.
