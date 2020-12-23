# 원격저장소 push시 오류

```bash
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/vandrager/project_test.gi
t'
#거절됨(rejected)
#원격저장소의 작업(커밋)이 로컬에 없음
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
#너는 원할거다
#원격 저장소의 변경사항을 먼저 통합하고
#예) git pull ...
hint: to the same ref. You may want to first integrate the remote changes
#다시 push
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

```

* 원격 저장소와 로컬 저장소의 커밋 히스토리를 확인하고 아래 명령어를 입력한다.

```bash
$git pull origin master
```

``` bash
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 704 bytes | 39.00 KiB/s, done.
From https://github.com/vandrager/project_test
 * branch            master     -> FETCH_HEAD
   07a5e45..446122e  master     -> origin/master
Merge made by the 'recursive' strategy.
 README.md | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)

```

* vim  편집기 창이 팝업될 것.

  * esc + wq(엔터)

    * w: write(저장)
    * q: qulit(나가기)

  * log를 확인한다.

    ``` bash
    git log --oneline
    #vim편집기가 뜬 이유 => 합쳐졌다라는 사실을 커밋으로 남김
    7351319 (HEAD -> master, origin/master) Merge branch 'master' of https://github.
    com/vandrager/project_test
    c827d2a a_plus
    446122e Update README.md
    07a5e45 Merge branch 'master' of https://github.com/vandrager/project_test
    6c1f8f4 add_test
    5c863ac Update README.md
    a81e059 Merge branch 'master' of https://github.com/vandrager/project_test
    63eade7 b-plus
    14bcce9 Create dv.txt
    d622b9d readme
    
    ```

    

