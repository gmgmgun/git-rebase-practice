## Git Command

- `git rebase [-i]`
  rebase는 현재 브랜치를 기반으로 다른 브랜치를 fast-forward 방식으로 merge한다.
  merge와 가장 큰 차이점은 서로 분기가 나누어진 브랜치 간 merge의 경우 3-way 방식으로 진행되어 merge commit이 발생되지만 rebase는 fast-forward로 진행되기 때문에 merge commit을 하지 않는다.
  각각 브랜치의 기존 커밋 히스토리를 유지한 채 새로운 커밋을 통해 병합하는 merge와 달리, rebase는 commit history를 선형적으로 변경시키기 때문에 이미 원격 레포지토리에 push된 커밋을 rebase할 경우 다른 팀원의 커밋과 충돌이 발생할 수 있으므로 미리 rebase를 하고 push 해야 한다.
  git rebase -i 의 경우 vim을 통해 커밋 히스토리를 재조정하거나 커밋 메시지를 수정하는 등 여러 작업을 수행할 수 있도록 한다. 예를 들어 squash 옵션으로 커밋을 통합하는 것도 가능하다.
  <br>
- `git rebase --abort`
  rebase를 진행하다 문제가 생기는 경우 abort 옵션을 통해 진행 중인 rebase를 취소할 수 있다.
  <br>
- `git rebase --continue`
  rebase를 진행하다 문제가 생기는 경우 문제를 해결하고 continue를 통해 rebase를 계속해서 진행할 수 있다.
  <br>
- `git reflog`
  레포지토리에서 이루어진 모든 작업의 로그를 보여주는 명령어다. 주로 레포지토리의 이력을 확인하고, 이전 커밋으로 돌아가기 위해 사용된다. 단, 로컬 레포지토리 한정으로 동작한다.
  <br>
- `git reset`
  가장 최근 커밋, 즉 HEAD 포인터의 위치를 변경시킬 때 사용하는 명령어다.
  세가지 모드가 있는데,
  1.'--soft'의 경우 변경 이력을 스테이지에 남기고 커밋을 되돌린다.
  2.'--mixed'의 경우 변경 이력을 스테이지에 남기지 않고 커밋을 되돌린다.
  3.'--hard'의 경우 변경 이력을 스테이지와 작업 디렉토리에서 삭제하고 커밋을 되돌린다.
