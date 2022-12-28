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

## 3.추가적으로 공부한 내용

>### (1) github 기반 원격저장소 활용

#### 명령어 정리

```bash
git clone <url> 원격 저장소 복제
git remote -v 원격 저장소 정보확인
git remote add <원격저장소> <url> 원격 저장소 추가
git remote rm <원격저장소> 원격 저장소 삭제
git push <원격저장소> <브랜치> 원격 저장소에 push
git pull <원격저장소> <브랜치> 원격 저장소로부터 pull
```

>### (2) gitignore

- 일반적인 개발 프로젝트에서 버전 관리를 별도로 하지않는 파일/디렉토리가 발생한다
- git 저장소에 .gitignore 파일을 생성하고 해당 파일이 버전에서 무시될 수 있게 한다
    * 특정 파일 : a.txt(모든 a.txt), test/a.txt(테스트폴더의 a.txt)
    * 특정 디렉토리 : /my_secret
    * 특정 확장자 : *.exe
    * 예외 처리 : !b.exe

>### (3) clone/push/pull
- clone : 원격저장소 복제
- push : 로컬저장소 커밋을 원격저장소로 보내기
- pull : 원격저장소 커밋 가져오기
    * 로컬에서 새로운 프로젝트를 시작할 경우 : git init
    * 원격에 있는 프로젝트 시작할 경우 : git clone
        * 협업 프로젝트, 외부 오픈소스 참여 등...
    * 프로젝트 개발 중 다른사람 커밋 받아올 경우 : git pull
    * 나의 로컬 프로젝트 개발 공유할 경우 : git push

