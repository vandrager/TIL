# Git 기초 문법

> 안녕하세요
>
> 아하아하
>
> > 꺽새">"이건 인용문을 사용할때 쓰는거구나
>
> Git은 분산형 버전관리시스템(DVCS)이다.

## Git 사전 준비

1. 윈도우) [git bash](https://gitforwindows.org/)를 설치한다.
2. 로컬 설정

``` bash
$ git config --global user.name 'vandrager'
$ git config --global user.email 'vandrager@naver.com'
```

* 처음 git을 설치하면, commit을 하는 작성자(Author)를 설정해야한다.
* email 정보는 github에 등록된 이메일을 설정하는 것을 추천
* 설정된 내용을 확인하기 위해서는 아래의 명령어를 입력한다.

``` bash
$git config --global -l
user.name=vandrager
user.email=vandrager@naver.com
```

* 오프라인 강의장에서 하는 경우 반드시 체크

# 기초 흐름

> 작업 => add => commit
>
> 작업이 끝나면, 커밋할 파일을 모아서(add), 커밋한다.(버전을 기록한다.)

### 0. 저장소 설정

``` bash
$git init
Initialized empty Git repository in C:/Users/vandr/OneDrive/바탕 화면/정리용/.gi
t/
(master) $

```

* git 저장소로 활용하기 위해서는 위의 명령어를 활용한다.
  * `#.git` 폴더가 생성
  * `(master)` 로 현재 작업중인 브랜치 확인



# 1. `add`

> 커밋을 위한 파일 목록(staging area)

```bash
$ touch test.txt
No commits yet
#트래킹이 되지 않는 파일 : WD O
Untracked files:
# git add 명령어를 사용!
# 커밋이 될 것에 포함시키기 위하여...
  (use "git add <file>..." to include in what will be committed)
        test.txt
#맨 마지막 줄 : 총 정리...
#nothing added to commit : staging area X
#untracked files present : WD 0
nothing added to commit but untracked files present (use "git add" to track)

```

* add 후 모습

``` bash
$git add .
$git status
On branch master

No commits yet
# 커밋이 될 변경사항 : SA O
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   test.txt

```

### 2. `commit`

> 버전을 기록(스냅샷)

``` bash
$git commit -m '커밋 메시지'
[master (root-commit) 901f817] 커밋 메시지
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test.txt
```

* 커밋 메시지는 현재 작업의 내용을 알 수 있도록 명확하게 작성한다.
* 커밋 이력을 확인하기 위해서는 아래의 명령어를 활용한다.

``` bash
$git log
commit 901f817cd3ee6834317e85c390eeb4ca966f3b26 (HEAD -> master)
Author: vandrager <vandrager@naver.com>
Date:   Tue Dec 22 14:36:15 2020 +0900
```

* 추가 옵션

``` bash
$git log -1
$git log --oneline
901f817 (HEAD -> master) 커밋 메시지
git log --oneline -1

$git log --oneline #한줄로 간단하게 보기
$git log --oneline -2 #최근 2개만 간단하게 보기
```

# 상태 확인

> git 저장소의 현재 상태는 status로 확인하는 습관을 가지자

``` bash
$git status
```

# Q&A, TIP

* git 앞에 안붙는 것은 그냥 윈도우 명령어
* 데이터 관련 직무 채용공고 분석



# Github 업로드

> github 홈페이지에서 + 누르고 새로운 저장소 만들기
>
> 저장소명은 무조건 영어로
>
> 설명(선택)에서는 한글로 설정해도 괜찮음
>
> 공개로 설정하고 바로 저장소 생성

* 작업 공간 폴더에서 bash 누르고 아래 명령어 입력

``` bash
$ git remote add origin https://github.com/vandrager/Project-test.git
#위는 프로젝트 명에 따라서 변동됨 remote 부분 복붙
$ git push origin master
```

