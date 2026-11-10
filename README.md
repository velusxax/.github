# velusxax/.github

VelusxaX 조직의 공통 설정 저장소입니다. 이 파일들은 VelusxaX의 **모든 저장소에 기본값으로 적용**됩니다. 어떤 저장소에 같은 종류의 파일이 따로 있으면 그 저장소의 파일이 우선합니다.

| 파일 | 역할 |
|---|---|
| [CONTRIBUTING.md](CONTRIBUTING.md) | 브랜치, 커밋, PR 규칙 |
| [PULL_REQUEST_TEMPLATE.md](PULL_REQUEST_TEMPLATE.md) | PR을 열 때 자동으로 채워지는 양식 |
| [ISSUE_TEMPLATE/](ISSUE_TEMPLATE/) | 기능 요청과 버그 이슈 양식 (빈 이슈는 막음) |
| [SECURITY.md](SECURITY.md) | 보안 문제 신고 방법 |
| [.github/workflows/check-commits.yml](.github/workflows/check-commits.yml) | 커밋 메시지 형식 검사 (각 저장소가 불러 쓰는 재사용 워크플로) |

> 기본값 적용은 GitHub 정책상 이 저장소가 **public**일 때만 동작합니다. 여기에는 코드나 비밀 정보 없이 규칙과 양식만 둡니다.

## 각 저장소에서 커밋 검사 사용하기

```yaml
# <저장소>/.github/workflows/commit-message.yml
name: commit-message
on: pull_request
jobs:
  check:
    uses: velusxax/.github/.github/workflows/check-commits.yml@main
```
