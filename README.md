# Git & Git Hub

## 1.Git 기본 명령어

- $git init : 로컬 저장소 생성
- $git add 파일명 : 파일추가(stage로 옮기는 것)
- $git commit -m : 버전으로 기록
- $git log : 현재 저장소에 기록된 커밋을 조회
- $git status : git 저장소에 있는 파일의 상태를 확인

## 2.Git Hub

>버전을 관리하고 개발자간 상호 협업이 가능 (원격저장소)

- push : 로컬 저장소 버전을 원격 저장소로 보낸다.
    ```bash
    $ git push origin master
    ```
    * 위의 명령어로 원격 저장소에 push
- pull : 원격 저장소의 버전을 로컬 저장소로 가져온다.
