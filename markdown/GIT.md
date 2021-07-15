# GIT

Git은 기본적으로 폴더를 관리해주는 것

관리할 폴더에 들어간 후

```
$ git init # initialize
$ git add . # 촬영 준비
$ git commit -m 'first commit' # 실제 촬영 -m : 메세지 
```

commit은 **스냅샷**을 찍었다고 보면 됨. 내가 관리할 폴더의 현재 상태 사진을 찍은 것.

> 참고 commit 이 안될 때 
  ```
  # 계정 초기 설정 또는 변경
  $ git config --global user.email "계정메일"
  $ git config --global user.name "계정이름"
  #git 설정 확인
  $ git config --global -l
  #(나갈 때는 Q)
  ```
> 참고 master 없애기(잘못된 곳에 init 했을 때)
  ``` 
  $ rm -rf .git
  ```

  절대 해서는 안될 일

  1. home folder에서 master가 뜨는 것(즉, 관리하지 않는 곳에서 master가 뜨는 것)
  2. 이미 관리하고 있는 폴더 내에서 폴더를 새로 만들고 들어간 후 git init하는 것

스냅샷이 제대로 됐는지 확인 하는 명령어

``` 
$ git log
```

내 폴더와 동기화 할 새로운 드라이브를 생성해야함. github의 repository

내 폴더와 repository 동기화하기

```
# 원격 저장소 등록(한번 등록하고 난 후 안해도 됨)
$ git remote add origin https://github.com/chaeb/TIL.git
  
# 등록된 원격 저장소 목록 확인
$ git remote -v
```

원격 저장소 업로드

```
$ git push origin master # 찍은 사진 upload
```

상태 확인

``` 
$ git status
```

변경 사항을 반영하고 싶을 때

``` 
# README.md 라는 새로운 파일 추가
$ touch README.md
$ open README.md # 열고 수정한 다음 저장

# 변경 사항 반영하기
$ git add . # 전부다 추가 할때는 .
$ git commit -m 'README.md 추가' # 변경사항 메세지 남기고 촬영하기
$ git push origin master # 변경사항 upload
```

하위 directory 추가

```
$ mkdir git
$ cd
$ touch 01_basic.md
$ open touch 01_basic.md
$ cd .. #상위 디렉토리로 옮겨가기

```

