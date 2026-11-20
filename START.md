# START — 볼트 세팅 절차 (Claude Code용)

사용자가 "START.md대로 볼트 세팅해줘"라고 하면 이 순서로 한다. 묻지 않고 기본값으로 만든다. 소속 · 프로젝트 같은 정보는 볼트에서 처음 `claude`를 열 때 볼트 `CLAUDE.md` "첫 실행" 절이 묻는다.

1. 볼트 경로를 정한다. 기본값은 사용자 폴더 아래 `Work`다.
   - Windows: `%USERPROFILE%\Work` (Claude Code에서는 `~/Work`)
   - WSL: Windows 사용자 폴더 아래 `/mnt/c/Users/<Windows 사용자>/Work`. Obsidian이 Windows에서 같은 폴더를 연다
   - macOS · Linux: `~/Work`
   - 사용자가 요청에 경로를 말했으면 그 경로를 쓴다.
2. 볼트 경로가 비어 있는지 확인한다. 파일이 있으면 멈추고 사용자에게 묻는다. 덮어쓰지 않는다.
3. `vault-template/`의 내용(`.obsidian/` 포함)을 볼트 경로로 복사한다.
4. 볼트 `CLAUDE.md`의 `{볼트 경로}` 칸만 1번 경로로 채운다. 다른 `{…}` 칸은 그대로 둔다(첫 실행 때 채움).
5. 볼트에서 `git init` 하고 첫 커밋을 한다. git `user.name` · `user.email`이 없으면 이 저장소에만(`git config` 전역 아님) 임시값 `worklog` · `worklog@localhost`로 커밋하고, 8번 안내에 적는다.
6. 저장소의 `examples/`는 볼트로 복사하지 않는다.
7. 결과를 확인한다: 볼트에 `.obsidian/plugins/calendar/main.js` · `periodic-notes/main.js`가 있는지, `git log`에 커밋이 하나 있는지.
8. 사용자에게 남은 일을 알린다.
   - Obsidian에서 볼트 폴더를 열고, 처음 뜨는 제한 모드 창에서 '커뮤니티 플러그인 켜기'를 누른다(플러그인은 이미 들어 있음).
   - 볼트 폴더에서 `claude`를 새로 열고 아무 말이나 하면 첫 실행 질문이 나온다.
   - 5번에서 임시 git 이름을 썼으면 그 사실.
