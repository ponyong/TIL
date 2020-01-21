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

git remote add [별칭] [git주소] <br>
ex) git remote add alice https:// ~~~~~~ .git

```
remote 한 저장소에 push 할 때 별명과 함께 push 명령어를 입력한다.
```

git push [별칭] <br>
ex) git push alice

## branch 분기 한 경우 커밋 및 Merge 방법

1. 내 branch에서 commit 까지 완료한다.

2. dev가 갱신 되었을수 있으므로 dev를 내 브랜치로 병합한다.
   feature를 활성화 하고 우클릭 + 현재 브랜치로 dev 를 병합
   이렇게 하면 feature가 최신화 되며 충돌 되는 파일을 알려준다.

3. 2번 단계에서 발생한 충돌을 모두 제거 한 후 다시 커밋 실행

4. 그 후 devlop으로 Merge Request 를 보내 Conflict가 나지 않으면 merge 승인

5. 그 후 dev에서 합쳐진 파일에서 이상이 없다면 master 로 릴리즈를 실행

