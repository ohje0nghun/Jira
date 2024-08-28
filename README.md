# Jira and Bitbucket 구성정보

현재 확인해야될 사항 및 진행사항

1. Bitbucket 기능 확인(Scripts Runner)
기능테스트 URL: http://sfmi-bitbucket.samsungfire.com/scm/pj20241380/sfmi-fw-jira-app.git

* 브랜치 명명 규칙 제약
- 현재 feature/SR-${NUMBER} 형식으로 브랜치를 생성하지 않으면 제약을 두도록 설정
- Bitbucket Scripts Runner 기능에 Pre-Check 스크립트 기능을 활용

* Merge Check 기능을 통한 PR 관리
- 생성된 PR에 대해서 Merged를 진행하기 위해서는 한명 이상의 reviewer에 승인이 필요하도록 제약 설정
- PR 생성 시 제약을 거는 부분은 현재 직접적인 기능이 없는 것으로 확인

- codemind 빌드유무에 따라 merge 승인이 되도록 제약 설정
- 현재는 빌드에 status 기준으로 설정되어있고 and codemind에 검사 결과 상태도 post형식으로 추가 테스트 필요




* 개발자 활동 목록 기능 있는지 확인
- 직접적인 기능은 없지만, commit, PR 등으로 확인가능 할것으로 예상

* PR중에 다른 소스변경이 있으면 이벤트로 처리할수 있는지
- 기본적으로 PR중에 develop 소스가 새버전으로 업데이트되면 아래 문구와 함께 merge 할수 없도록 기능제공
You are attempting to modify a pull request based on out-of-date information.
- 경고나 안내 문구에 대해서는 scripts runner 기능을 통해 구성할 수 있는것으로 확인





2. Jira 
기능 테스트 URL:  http://sfmi-jira.samsungfire.com

* 이슈 발행 시 Bitbucket 브랜치 생성 자동화
- 현재 프로젝트 feature/${키값-이슈등록번호} 형식으로 이슈 발행 시 브랜치가 생성되도록 설정
- Jira 이슈 발행을 통해 생성된 브랜치와 분기점 생성을 진행하기 위해선 이슈 키값을 브랜치에 등록
해야 되는 조건이 있어 브랜치 관련 alias 설정 부분에 대해서 문제가 있을 수 있음.
-> 해결

* 변경 접수 관련 대시보드 생성(IT Space)
확인필요



