

# git 사용법

### git config

- `$ git config --global user.name "____" `
  - 이름 전역 설정

- $ git config --global user.email `____@gmail.com`
  - 이메일 전역 설정

- $ git config --global -l
  - 전역으로 config 된 목록 확인
- $ git config --unset --global username
  - 전역으로 설정된 이름 삭제

### git init `(master)`

- 저장소 설정
- 주의사항
  - 이미 git 저장소인 폴더 내에 또 다른 git 저장소를 만들지 않는다.
  - home dir에서 사용시 복잡해질수 있다.



##### (Woking Directory -> Staging Area -> Commits)순서로 이동

### git status

- working dir와 staging area에 있는 파일의 상태 파악



### git add

- `$ git add .` `$ git add 파일명` 을 이용하여 working dir의 파일을 Staging Area 로 이동

### git commit

- `$ git commit -m ___`  ___에는 commit 제목
- staging area의 파일을 commits로 이동

### git log 

- git의 log 확인

- `$ git log --oneline` 현재 헤더,커밋 파악 가능

### git remote

- 원격 저장소 관리 명령어

- `$ git remote add <저장소이름orgin><주소>`

- `$ git remote -v` : 저장소 확인



### git push

- commit 된 파일을 원격 저장소에 올림

- `$ git push -u <저장소 이름 orgin> <브랜치 이름 master>`

  

### .gitignore

- 특정 파일 혹은 폴더에 대해 git이 관리 하지 못하도록 지정하는 방법
- 주의사항
  1. 파일 이름은 `.gitignore` 로 해야함
  2. git add 전에 작성해야함
  3. `.git`파일과 같은 위치에 생성해야함

- gitignore.io를 활용하자

### git clone

- `git clone <주소>` 
- 원격 저장소의 commit 내역을 가져와 로컬 저장소를 생성
- 주의사항
  1. git init, git remote add가 이미 적용되어있음
  2. desktop/til 이라는  폴더에 til이름의 폴더를 받을시 desktop/til/til 폴더가 생성이됨

- `git clone 주소 abc`으로 입력시 abc라는 폴더로 생성



### git pull

- 원격 저장소의 변경 사항을 가져와서 로컬 저장소를 업데이트 하는 명령어
- `$ git pull <저장소이름><브랜치 이름>`
- `$ git pull origin master`
- pull 하기 전에 commit 해서 같은 라인 충돌시 어느 내용을 반영할지 선택해야함



### branch

- 작업 공간을 독립적으로 작업 할 수 있도록 도와주는 도구
- `$ git branch` 브랜치 목록 확인
- `$ git branch -r` 원격 저장소의 브랜치 목록 확인
- `$ git branch <브랜치이름>` 새로운 브랜치 생성
- `$ git branch <브랜치이름><커밋 ID>` 특정 커밋 기준으로 브랜치 생성
- `$ git branch -d <브랜치이름>` 병합된 브랜치 삭제
- `$ git branch -D <브랜치이름>` 브랜치 강제 삭제



### git switch

- 현재 브랜치에서 다른 브랜치로 head를 이동시키는 명령어
- `$ git switch <브랜치이름>`
- 주의사항 : test.txt를 만들고 git add를 하지 않은 상태에서 다른 브랜치로 스위치시 스위치한 폴더에 test.txt가 생성됨

### git checkout <브랜치 이름>

### git merge `<commit>`     브랜치 병합



### code . 

- 그 폴더에서 code 실행
