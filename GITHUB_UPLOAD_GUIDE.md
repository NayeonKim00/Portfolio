# GitHub Upload Guide

이 폴더는 하나의 포트폴리오 저장소로 올리는 구성을 기준으로 정리되어 있습니다.

## Option A. Git 설치 없이 웹에서 업로드

1. [GitHub](https://github.com)에 로그인합니다.
2. 오른쪽 위 `+` 버튼에서 `New repository`를 선택합니다.
3. Repository name 예시: `quant-finance-portfolio`
4. 공개 범위를 `Public` 또는 `Private`로 선택합니다.
5. 이미 이 폴더에 `README.md`가 있으므로 `Add a README file`은 체크하지 않는 편이 깔끔합니다.
6. 저장소 생성 후 `uploading an existing file` 또는 `Add file > Upload files`를 누릅니다.
7. `C:\Users\HI\Desktop\깃허브에 넣을 포트폴리오` 안의 모든 파일과 폴더를 드래그해서 업로드합니다.
8. 아래 Commit message 예시를 입력하고 `Commit changes`를 누릅니다.

대용량 생성 파일 `monthly_panel_data.csv`는 GitHub 100MB 제한을 넘어서 업로드 폴더 밖의 로컬 보관 폴더로 분리했습니다.

```text
C:\Users\HI\Desktop\깃허브에 넣을 포트폴리오_local-large-files
```

```text
Organize quant finance portfolio projects
```

## Option B. Git 설치 후 명령어로 업로드

현재 PowerShell에서는 `git` 명령을 찾지 못했습니다. 명령어 방식을 쓰려면 먼저 [Git for Windows](https://git-scm.com/download/win)를 설치한 뒤 PowerShell을 새로 열어주세요.

```powershell
cd "C:\Users\HI\Desktop\깃허브에 넣을 포트폴리오"
git init
git config user.name "NayeonKim00"
git config user.email "ky24918@sogang.ac.kr"
git add .
git commit -m "Organize quant finance portfolio projects"
git branch -M main
git remote add origin https://github.com/NayeonKim00/<repo-name>.git
git push -u origin main
```

`<repo-name>`은 GitHub에서 만든 저장소 이름으로 바꾸면 됩니다. 예시는 `quant-finance-portfolio`입니다.

GitHub는 비밀번호를 이용한 `git push` 인증을 지원하지 않습니다. 명령어 방식으로 올리려면 GitHub Personal Access Token 또는 GitHub CLI/browser login을 사용해야 합니다.

## 프로젝트별 개별 저장소로 올리고 싶을 때

각 프로젝트를 별도 저장소로 운영하려면 아래 폴더 중 하나만 새 저장소에 업로드하면 됩니다.

- `01-risk-management`
- `02-derivatives`
- `03-team-projects`
- `04-paper-replication`

단, 공통 실행 환경 파일인 `requirements.txt`가 필요하면 해당 프로젝트 저장소에도 복사해서 함께 올리는 것을 권장합니다.
