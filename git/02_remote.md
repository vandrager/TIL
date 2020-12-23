# 원격 저장소 활용

> 원격 저장소(remote repository)를 제공하는 서비스는 github, gitlab, bitbuket 등이 있다.



## 1. 원격저장소 설정하기

```bash 
$git remote add origin ___
```

* 깃아, 원격 저장소를 추가해줘.(add) origin이라는 이름으로 URL을!!

* 원격저장소  설정을 삭제(remove)하는 명령어는 다음과 같다.

  ```bash
  $ git remote rm origin
  ```

## 2. 원격 저장소 확인하기

```bash
$git remote -v
origin  https://github.com/vandrager/Project-test.git (fetch)
origin  https://github.com/vandrager/Project-test.git (push)
```

### 3. `push` 

```bash
$git push origin master

Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (7/7), 570 bytes | 570.00 KiB/s, done.
Total 7 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/vandrager/Project-test.git
 * [new branch]      master -> master
```

* `origin`저장소의  `master`브랜치로 `push`



# 4.pull

* 원격 저장소의 변경 사항을 받아옴

``` bash
$git pull origin master
```

# 5. clone

* 원격 저장소를 복제함

``` bash
$git clone ____
```



# 업데이트 하려면?

``` bash
$git remote -v
원격 저장소 위치 확인
$ git add .(넣고 싶은 것을 추가)

$ git commit -m 'add readme'
#새로운 것을 커밋해줌
$ git push origin master
#push로 업데이트해줌
```

# 상대경로 설정(md에서)

``` bash
#[마크다운 활용법](./git/마크다운_문법.md)
```



# 명령어 정리

>  git init           
>
>  git status
>
> git add . 
>
> git commit -m '메시지' 
>
> git log
>
> git remote add origin 
>
> git remote -v
>
> git push origin master



# 참고하면 좋을 블로그

> 프로그래밍 할 때 네이밍, 약속 시 참고하면 좋다.

https://blog.ull.im/engineering/2019/03/10/logs-on-git.html

https://meetup.toast.com/posts/106

> 나만의 블로그 만들기
>
> github pages => 저장소를 html 홈페이지로 제작

* 깃허브 새로운 저장소 생성(이름은 (내아이디.github.io)로 반드시 설정해야함)
* 다른 내용은 동일함

1. *<u>Jekyll - 과거부터 많이 사용</u>*
2. **Gatsby - 최근 핫한 기술이 많이 들어감**
3. [스타트붓스트랩](https://startbootstrap.com/)

마크다운 문법으로 작성된 것을 html + css + js 템플릿으로 만들어줌

github  > 오픈소스, 프로젝트, TIL

Markdown: 다양한 정리, 문서작업

=> README.md 써보시는 것을 추천

(무슨 내용인지 얘기해주는 소개글 느낌)







