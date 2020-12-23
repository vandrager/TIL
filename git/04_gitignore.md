# gitignore

> git으로 관리하지 않을 파일/폴더를 관리
>
> `.gitigmore` 파일을 생성하여 아래와 같이 작성한다.
>
> ​	**메모장에서 편집 금지!!**
>
> ``` bash
> data.csv #특정 파일
> *.png #특정 확장자(png확장자인 모든 것)
> secret/ #특정 폴더
> !profile.png #모든 png는 빼고, profile.png는 넣고!
> ```

* 보통 OS (windows/mac), 개발환경(IDE, text editor), 특정 언어에서 발생하는 파일/폴더들 관리
* text editor = vscode같은 코드 편집기를 말함
* ide는 통합개발환경(ex. 이클립스, 파이참)
* http://gitignore.io 에서 조건에 맞게 검색
  * 예) 자바로 eclipse로 윈도우에서 개발하고 있다.
  * 파이썬을 vscode로 윈도우에서 개발하고 있다.
    * https://www.toptal.com/developers/gitignore/api/windows,python,vscode
  * or https://github.com/github/gitignore참고

# 다른 사람의 git 파일 업데이터 요구시

1. 타인의 코드 클론 클립보드 복사

``` bash
$git clone "클립보드 내용 복붙"

```

2. 압축파일 다운로드 경우에는 history까지 복사되진 않는다. 단순히 최신 상태의 파일 목록만 다운로드 된다.



# DVCS와 CVCS 차이점

git은 분산버전관리 시스템으로 우수한 연결성

업데이트 및 history까지 모두 기억하고 있다.

중앙서버의 경우 history까지 저장X

