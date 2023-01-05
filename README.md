# TIL

## 목차
## [1. Git 기본 명령어](#1-git-기본-명령어)
## [2. 명령어 정리](#명령어-정리)
## [3. 마크다운 문법](#마크다운-문법)
## [4. Python 기초](#python-기초)

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

# 마크다운 문법

## 마크다운?
- 텍스트 기반의 가벼운 마크업 언어

    * 마크업 언어 : HTML/CSS 문서의 구조화
- text to html 으로의 변형

## 활용예시
- README.md
- 정정사이트생성기 기반 블로그
- 마크다운 기반 SW(Jupyer notebook, Notion)

## 문서제목 설정하기
- Heading : 문서의 제목/소제목

    * #의 개수에 따라 대응되는 수준 (H1~H6까지 표현가능)
    H6으로 갈수록 크기가 작아진다

## List : 목록
- 순서가 있는 (ol)과 순서가 없는 (ul)로 구성
- Tab으로 하위항목 구성이 가능
    
    * 다시 돌아올때 : shift + Tab

## 텍스트 강조하기
- 2022년 최고의 밈 **중꺾마**

    * 문자 기울이기 : *

    * 문자 진하게 : **

    * 취소선 : ~~

# Python 기초

## Python
- 파이썬이란?
    * 다른 프로그래밍 언어보다 문법이 간단하고 엄격하지 않음
- Expressive Language
    * 같은 작업에 대해서도 C나 자바로 작성할 때 보다 더 간결하게 작성 가능
- 크로스 플랫폼 언어
    * 다양한 운영체제에서 실행가능

## 파이썬의 특징
- 인터프리터 언어
    * 소스코드를 기계어로 변환하는 컴파일 과정없이 바로 실행가능
    ```bash
    >>> 2 + 2 # 사용자가 입력 (input)
    4         # 컴퓨터가 대답 (output)
    ```
- 객체 지향 프로그래밍(Object Oriented Programming)
    * 파이썬은 객체지향 언어이며, 모든 것이 객체로 구현되어 있음
        * 객체(object) : 숫자, 문자, 클래스 등 값을 가지고 있는 모든 것

## 객체와 변수
### 변수(Variable)
- 변수는 할당 연산자(=)를 통해 값을 할당
- type() : 변수에 할당된 값의 타입

### 객체의 종류
1. 수치형(Numeric Type)
- 정수(Int)
    * 모든 정수 타입은 int
    * 매우 큰 수를 나타낼 때 오버플로우가 발생하지 않음
- 실수(Float)
    * 정수가 아닌 모든 실수는 float 타입
2. 불린형(Boolean Type)
- True/False 값을 가진 타입은 bool
    * True는 1, False는 0
- 비교/논리 연산을 수행함에 있어서 활용

## 연산자(Operater)
1. 산술 연산자
- 기본적인 사칙연산 및 수식 계산
2. 복합 연산자
- 연산과 할당이 함께 이뤄짐
3. 비교 연산자
- 값을 비교하며, True / False 값을 리턴함
4. 논리 연산자
- 논리식을 판단하여 True와 False를 반환함
    * and : 모두 참인 경우 참, 그렇지 않으면 거짓
    * or : 둘 중 하나만 참이라도 참, 그렇지 않으면 거짓
    * not : 참, 거짓의 반대의 결과
    ```bash
    num = 100
    num >= 100 and num % 3 == 1
    # True
    ```

## 컨테이너
### 컨테이너란?
- 여러 개의 값을 담을 수 있는 것(객체)
- 컨테이너의 분류
    * 순서가 있는 데이터(ordered) vs 순서가 없는 데이터(unordered
    )
### 컨테이너 분류
- 시퀀스
    * 문자열 : 문자들의 나열
    * 리스트 : 변경 가능한 값들의 나열
    * 튜플 : 변경 불가능한 값들의 나열
    * 레인지 : 숫자의 나열
- 컬렉션/비시퀀스
    * 세트 : 유일한 값들의 모음
    * 딕셔너리 : 키-값들의 모음
### 문자열(String Type)
- 모든 문자는 str 타입
- 문자열은 작은 따옴표(')나 큰 따옴표(")를 활용하여 표기
- 결합(Concatenation)
    ```bash
    'hello, ' + 'python!'
    # 'hello, python!'
    ```
- 반복(Repetition)
    ```bash
    'hi!' * 3
    # 'hi!hi!hi!'
    ```
- 포함(Membership)
    ```bash
    'a' in 'apple'
    # True
    'app' in 'apple'
    # True
    'b' in 'apple'
    # False
    ```
### 리스트(List)
- 변경 가능한 값들로 나열된 자료형
- 순서를 가지며, 서로 다른 타입의 요소를 가질 수 있음
- 변경 가능하며, 반복 가능함
- 항상 대괄호 형태로 정의하며, 요소는 콤마로 구분

### 리스트 접근과 변경
```bash
# 값 접근
a = [1, 2, 3]
print(a[0])
# 1

# 값 변경
a[0] = '1'
print(a)
# ['1', 2, 3]
```
### 리스트 값 추가/삭제
- 값 추가는 .append()를 활용하여 추가하고자 하는 값을 전달
```bash
even_numbers = [2, 4, 6, 8]
even_numbers.append(10)
even_numbers
# => [2, 4, 6, 8, 10]
```
- 값 삭제는 .pop()을 활용하여 삭제하고자 하는 인덱스를 전달
```bash
even_numbers = [2, 4, 6, 8]
even_numbers.pop(0)
even_numbers
# => [4, 6, 8]
```

## 제어문
- 파이썬은 기본적으로 위에서부터 아래로 순차적으로 명령을 수행
- 특정 상황에 따라 코드를 선택적으로 실행(분기/조건)하거나 계속하여 실행(반복)하는 제어가 필요

## 조건문
- 조건문은 참/거짓을 판단할 수 있는 조건식과 함께 사용

### 조건문 기본 형식
- expression에는 참/거짓에 대한 조건식
    * 조건이 참인 경우, 이후 들여쓰기 되어있는 코드 블럭 실행
    * 이외의 경우(거짓), else이후 들여쓰기 되어있는 코드 블럭 실행
    ```bash
    if <expression>:
        # run this code
    else:
        # run this code
    ```
    ```bash
    a = -10
    if a >= 0:
        print('양수')
    else:
        print('음수')
    print(a)  # >> (음수)
    ```
### 복수 조건문
- 복수의 조건식을 활용할 경우 elif를 활용하여 표현
```bash
if <expression>:
    # code block
elif <expression>:
    # code block
elif <expression>:
    # code block
else:
    # code block
```
### 중첩 조건문
- 조건문은 다른 조건문에 중첩되어 사용될 수 있음
    * 들여쓰기를 유의하여 작성 !!
    ```bash
    if <expression>:
        # code block
        if <expression>:
            # code block
    else:
        # code block
    ```
### range
- 숫자의 시퀀스를 나타내기 위해 사용
    * 기본형 : range(n)
        * 0 부터 n-1 까지의 숫자의 시퀸스
    * 범위 지정 : range(n,m)
        * n 부터 m-1 까지의 숫자의 시퀸스
    * 범위 및 스텝 지정 : range(n,m,s)
        * n 부터 m-1 까지 s 만큼 증가시키는 숫자의 시퀀스
- 변경 불가능하며(immutable), 반복 가능함(iterable)

## 반복문
- 특정 조건을 도달할 때까지, 계속 반복되는 일련의 문장

### 반복문의 종류
- while문
    * 종료조건에 해당하는 코드를 통해 반복문을 종료시켜야 함
- for문
    * 반복가능한 객체를 모두 순회하면 종료(별도의 종료조건이 필요없음)
- 반복 제어
    * break, continue, for-else

### while문
- while문은 조건식이 참인 경우 반복적으로 코드를 실행
    * 조건이 참인 경우 들여쓰기 되어있는 코드 블록이 실행됨
    * 코드 블록이 모두 실행되고, 다시 조건식을 검사하며 반복적으로 실행됨
    * while문은 무한 루프를 하지 않도록 종료조건이 반드시 필요

### for문
- for문은 시퀀스(string, tuple, list, range)를 포함한 순회가능한 객체요소를 모두 순회함
    * 종료조건 필요없음
```bash
chars = input() > hi
for char in chars:
    print(char)
h
i
```
### 반복문 제어
- break : 반복문을 종료
- continue : continue 이후의 코드블록은 수행하지 않고, 다음 반복을 수행
- for-else : 끝까지 반복문을 실행한 이후에 else문 실행
    * break를 통해 종료되는 경우 else문은 실행되지 않음
    
