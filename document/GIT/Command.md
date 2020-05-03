# GIT 주요 커맨드 정리

## 설정 및 초기화

```
사용자명 / 이메일 전역 설정
```

git config --global user.name "Your name" <br>
git config --global user.email "Your email" <br>

## 기본 명령어

```
현재 상태 보기
```

git status

```
unstage -> stage 상태로 변환
```

git add <파일> <br>
git add . // 모든 파일 <br>

```
commit 상태로 변경
```

git commit -m "커밋메세지"

```
커밋 메세지를 여러줄로 작성하는 법
```

commit -m 후에 여는 따옴표 " 후에 닫히는 따옴표를 만나기전 엔터는 개행으로 처리 된다.

```
마스터에서 최신버전 갱신
```

git pull

```
커밋 내용을 포함한 최신 버젼 갱신
```

git push

## remote 설정 하는 법

```
현재 원격 저장소의 상태를 확인한다.
```

git remote -v

```
remote 할 저장소를 별명과 함께 설정한다.
```

git remote add [별칭][git주소] <br>
ex) git remote add alice https:// ~~~~~~ .git

```
remote 한 저장소에 push 할 때 별명과 함께 push 명령어를 입력한다.
```

git push [별칭] <br>
ex) git push alice

## branch 분기 한 경우 커밋 및 Merge 방법

1. 새로운 작업 브랜치를 생성한다.

```
git branch

현재 있는 branch list를 확인한다.


git branch 브랜치 이름

git branch test

test 라는 브랜치를 생성한다.
```

2. 생성한 브랜치로 이동한다.

```
git checkout test
```
