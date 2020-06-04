## EC2에 백엔드 서버 배포하는 방법에 대해 기술 합니다.

### Back End Publish

```

1. Putty 에서 ec2 서버에 접속.

2. Spring 콘솔 창에 gradlew build를 통해 .jar 파일 생성

3. WinSCP를 통해 경로에 .jar 파일 옮기기

4. putty 실행 창에서 실행 시키고 , 백그라운드에서 돌리기 위해 다음과 같은 명령어 실행


```

```javascript
    java -jar catdog-1.0-SNAPSHOT.jar   // 일반 실행
    nohup java -jar catdog-1.0-SNAPSHOT.jar &  // 백그라운드 실행
```

nohup 명령어를 사용하면 사용한 디렉토리에 nohup.out이라는 파일이 생성된다.

이 파일에는 nohup로 실행하는 명령의 출력이 기록되어 진다.

만약 생성하고 싶지 않다면 /dev/null 에 출력하도록 하면 된다

```javascript
# nohup echo hello > /dev/null
```

# 중지하는 방법

```javascript
# ps -ef | grep a.out // pid 찾기
# kill -9 PID번호     // 찾은 pid를 통해 프로세스 종료
```
