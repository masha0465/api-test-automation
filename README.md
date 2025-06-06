# api-test-automation

* API 테스트 자동화 설계

  Postman에서 pnp_api의 주요 엔드포인트(로그인, 데이터 조회, 등록 등)를 컬렉션으로 구성

  각 요청에 대해 테스트 스크립트 및 Pre-request Script 작성 (예: 인증 토큰, 동적 변수 처리)

  환경(Environment) 파일을 활용해 base_url, 토큰 등 환경별 변수 관리


* 수동 테스트 → 자동화 전환

  Postman Collection Runner로 반복 테스트 및 데이터 기반 테스트 수행

  컬렉션과 환경 파일을 JSON으로 내보내 Newman에서 활용


* Newman 기반 커맨드라인 자동화

  Newman을 전역 설치(npm install -g newman)

  커맨드라인에서 컬렉션 자동 실행 및 다양한 리포트(HTML 등) 생성

  실패 시 로그 및 상세 리포트로 원인 분석


* CI/CD 파이프라인 구축

  GitHub에 저장소 생성 및 버전 관리 체계 수립

  .github/workflows에 Newman 실행 워크플로우(YAML) 작성

  코드 변경(push, PR) 시마다 자동으로 API 테스트가 실행되도록 GitHub Actions 연동
 
  원격 저장소와 로컬 저장소 동기화, 권한 관리, 충돌 해결 등 Git 기본기 습득
