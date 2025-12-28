## <img src="https://img.icons8.com/color/1200/tableau-software.jpg" width="25" height="25"/> Tableau Developer

이 저장소는 **Tableau 개발자 관점**에서 활용 가능한 기술과 실무 예제를 정리한 공간이다.  
운영 자동화, 데이터 관리, 거버넌스, 모니터링 관점에서 **API 기반 Tableau 활용**에 초점을 둔다.

---
## 🗂️ Tableau Developer 개요

- [Tableau REST API](#tableau-rest-api-개요) [[공식 문서]](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api.htm?_gl=1*10ycje4*_gcl_au*MTUzMjIwNDM5OS4xNzY1MTk3NjQx*_ga*MTQxNTE1NTQ1NC4xNzY1MTk3NjQy*_ga_8YLN0SNXVS*czE3NjU4MDIwMDIkbzIkZzEkdDE3NjU4MDIxNjUkajYwJGwwJGgw)
- Tableau Extension API [[공식 문서]](https://tableau.github.io/extensions-api/docs/)
- Tableau Hyper API [[공식 문서]](https://tableau.github.io/hyper-db/docs/)
- Tableau Meta Data API [[공식 문서]](https://help.tableau.com/current/api/metadata_api/en-us/index.html?_gl=1*1fcf5zh*_gcl_au*MTUzMjIwNDM5OS4xNzY1MTk3NjQx*_ga*MTQxNTE1NTQ1NC4xNzY1MTk3NjQy*_ga_8YLN0SNXVS*czE3NjU4MDIwMDIkbzIkZzEkdDE3NjU4MDIyNDMkajU2JGwwJGgw)
- Tableau JavaScript API [[공식 문서]](https://help.tableau.com/current/api/js_api/en-us/JavaScriptAPI/js_api.htm?_gl=1*f9ov33*_gcl_au*MTUzMjIwNDM5OS4xNzY1MTk3NjQx*_ga*MTQxNTE1NTQ1NC4xNzY1MTk3NjQy*_ga_8YLN0SNXVS*czE3NjU4MDIwMDIkbzIkZzEkdDE3NjU4MDIyMTUkajEwJGwwJGgw)
- Tableau Connector SDK [[공식 문서]](https://tableau.github.io/connector-plugin-sdk/docs/)
- Tableau Analytical Extension API [[공식 문서]](https://tableau.github.io/analytics-extensions-api/docs/ae_intro.html)
- Tableau Web Data Connector [[공식 문서]](https://tableau.github.io/webdataconnector/docs/)
- Tableau Document API Python [[공식 문서]](https://tableau.github.io/document-api-python/)
- Tabpy [[공식 문서]](https://tableau.github.io/TabPy/)
- R [[공식 문서]](https://help.tableau.com/current/pro/desktop/ko-kr/r_connection_manage.htm?_gl=1*1m9yxgk*_gcl_au*MTUzMjIwNDM5OS4xNzY1MTk3NjQx*_ga*MTQxNTE1NTQ1NC4xNzY1MTk3NjQy*_ga_8YLN0SNXVS*czE3NjU4MDIwMDIkbzIkZzEkdDE3NjU4MDI0OTAkajMzJGwwJGgw)

---

## Tableau REST API 개요

**Tableau REST API**는 Tableau Server / Tableau Cloud의 리소스를  
**HTTP 기반 API**로 제어할 수 있도록 제공되는 공식 인터페이스이다.

UI에서 수행하던 대부분의 관리·운영 작업을 코드로 자동화할 수 있다.

공식 참고 문서 : [Tableau REST API Help](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api.htm)

---

## 🎯 REST API로 할 수 있는 주요 작업

### 1️⃣ 인증 및 세션 관리
- Personal Access Token(PAT) 기반 인증
- 사이트(Site) 단위 세션 관리
- 토큰 만료 및 재인증 처리

### 2️⃣ 콘텐츠 관리
- 프로젝트(Project) 생성 / 이동
- 워크북(Workbook) 배포 및 삭제
- 데이터 원본(Data Source) 조회 및 관리
- 추출(Extract) 새로고침 상태 확인

### 3️⃣ 사용자 & 그룹 관리
- 사용자(User) 조회 및 추가
- 그룹(Group) 생성 및 사용자 할당
- 라이선스 타입 확인 및 관리

### 4️⃣ 운영 및 모니터링
- 추출 / Flow 실행 이력 조회
- 실패 로그 및 상태 코드 분석
- Tableau Cloud 운영 현황 자동 수집

---

## 🧱 기본 API 구조

REST API는 아래와 같은 공통 구조를 가진다.

```text
https://<tableau-server>/api/<api-version>/sites/<site-id>/<resource>
```

예시
```text
GET /api/3.21/sites/{site_id}/workbooks
```